# Suppression du suport de certains navigateurs (BP040)

## Règle

:recycle: CreateReactApp propose une intégration à browserlist qui nous permet d'inclure le code js nécessaire pour supporter l'ensemble des navigateurs du marché.
Cependant, les applications AXA ont pour cible un parc de navigateurs limités (suppression du support IE), nous pouvons, donc, optimiser le nombre de navigateurs dans le browserlist.

## Gains

Optimisation de la taille des ressources statiques.

## Valider la mise en place de la bonne pratique

:x: Code à éviter

```js
 "production": [
      ">0.2%",
    ],
```

:heavy_check_mark: Code à favoriser (à optimiser en fonction des navigateurs supportés par votre application)

```js
 "production": [
      ">0.2%",
      "not dead",
      "not op_mini all"
    ],
```

Points de contrôle

- [ ] Vérifier dans le package.json
- [ ] Vérifier dans le .browserslistrc

## Liens

- [Testez votre configuration](https://browsersl.ist)
- [Github de la librairie](https://github.com/browserslist/browserslist)
