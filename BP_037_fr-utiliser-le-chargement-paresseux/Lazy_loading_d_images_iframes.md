\newpage

# Images/iframes Lazy Loading (BP037)

## Platform

|   OS          |  OS version  |  Langage   |
|---------------|--------------|------------|
| -             | -            | HTML       |

## Main caracteristics

|   ID     | Title                       | Category      | Sub-category   |
|----------|-----------------------------|---------------|----------------|
| CRDOMxxx | Images/iframes Lazy Loading | Best Practice | -              |

## Severity / Remediation Cost

- **Case 1**: Images Lazy Loading
  
|  Severity  | Remediation Cost    |
|------------|---------------------|
| Medium     | Medium              |

- **Case 2**: Iframes Lazy Loading

|  Severity  | Remediation Cost    |
|------------|---------------------|
| Medium     | Medium              |

## Rule short description

- **Case 1**: Images Lazy Loading
- **Case 2**: Iframes Lazy Loading

## Rule complete description

## Text

:recycle: Modern browsers allow to load images when the user is just about to see them, for example when the image is at the bottom of the page and needs to scroll down to be displayed.
If you want to make this feature available on older browsers (i.e. IE), a `polyfill` will be needed.
You will also need to specify the width and height attributes:
https://stackoverflow.com/a/67552400

Benefits: Optimization of the size of static resources.

[Working example with images](https://mathiasbynens.be/demo/img-loading-lazy)

[Working example with iframes](https://lazy-load.netlify.app/iframes)

### Links

- [Lazy loading images](https://developer.mozilla.org/en-US/docs/Web/Performance/Lazy_loading#images_and_iframes)
- https://web.dev/browser-level-image-lazy-loading/
- [Lazy loading for videos](https://web.dev/lazy-loading-video/)

## HTML

:x: Code to avoid

```html
<img src="image.jpg" alt="..." />
<iframe src="video-player.html" title="..."></iframe>
```

:heavy_check_mark: Recommended code

```html
<img src="image.jpg" alt="..." loading="lazy" width="200" height="200" />
<iframe
  src="video-player.html"
  title="..."
  loading="lazy"
  width="200"
  height="200"
></iframe>
```

## Implementation principle

- [ ] On the `img` or `iframe` tag, check usage of the following attribute : `loading="lazy"`
- [ ] On the `img` or `iframe` tag, check usage of the following attribute : `width=...`
- [ ] On the `img` or `iframe` tag, check usage of the following attribute : `height=...`
