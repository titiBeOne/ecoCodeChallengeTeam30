# Images/iframes Lazy Loading (BP037)

## Rule

:recycle: Modern browsers allow to load images when the user is just about to see them, for example when the image is at the bottom of the page and needs to scroll down to be displayed.
If you want to make this feature available on older browsers (i.e. IE), a `polyfill` will be needed.
You will also need to specify the width and height attributes:
https://stackoverflow.com/a/67552400

[Working example with images](https://mathiasbynens.be/demo/img-loading-lazy)

[Working example with iframes](https://lazy-load.netlify.app/iframes)

## Benefits

Optimization of the size of static resources.

## How to validate the implementation of the best practice

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

Checklist

- [ ] On the `img` tag, check usage of the following attributes : `loading="lazy"`, `width`, `height`.

## Links

- [Lazy loading images](https://developer.mozilla.org/en-US/docs/Web/Performance/Lazy_loading#images_and_iframes)
- https://web.dev/browser-level-image-lazy-loading/
- [Lazy loading for videos](https://web.dev/lazy-loading-video/)
