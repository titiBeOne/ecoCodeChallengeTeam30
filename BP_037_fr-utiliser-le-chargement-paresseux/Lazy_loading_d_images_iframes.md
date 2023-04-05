# Lazy Loading d'images/iframes (BP037)

## Règle

:recycle: Les navigateurs modernes permettent de charger des images seulement lorsque l'utilisateur est sur le point de les voir, par exemple : quand l'image est en bas de page et nécessite un scroll pour être affichée.
Si vous souhaitez que cette fonctionnalité soit disponible sur des anciens navigateurs (ie), un `polyfill` sera nécessaire pour son bon fonctionnement.

## Gains

Optimisation de la taille des ressources statiques.

## Valider la mise en place de la bonne pratique

:x: Code à éviter

```html
<img src="image.jpg" alt="..." />
<iframe src="video-player.html" title="..."></iframe>
```

:heavy_check_mark: Code à favoriser

```html
<img src="image.jpg" alt="..." loading="lazy" />
<iframe src="video-player.html" title="..." loading="lazy"></iframe>
```

Points de contrôle

- [ ] Vérifiez l'utilisation de l'attribute `loading="lazy"` sur les balises `img`

## Liens

- [Lazy loading images](https://developer.mozilla.org/en-US/docs/Web/Performance/Lazy_loading#images_and_iframes)
- https://web.dev/browser-level-image-lazy-loading/
- [Lazy loading sur les vidéos](https://web.dev/lazy-loading-video/)


