# Optimiser l'utilisation de Lodash (BP040)

## Règle

:recycle: Lodash est une librairie JavaScript très utilisée pour ses différentes utilitaires. Mais la plupart du temps,
nous importons l'ensemble de la librairie, pour une seule méthode utilisée ce qui alourdit le poids de la page.

Nous pouvons plutôt utiliser les modules JavaScript spécifiques pour chaque méthode exposée par la librairie (par exemple le module `lodash/map` si vous souhaitez utiliser la méthode `map` ou directement la fonction

De plus, avant d'utiliser Lodash, assurez-vous qu'une méthode similaire n'existe pas nativement en JavaScript.

## Gains

Optimisation de la taille des ressources statiques.

## Valider la mise en place de la bonne pratique

:x: Code à éviter

```js
import _ from "lodash";

_.map([4, 8], n => n * n);
```

:heavy_check_mark: Code à favoriser

```js
import map from "lodash/map";

map([4, 8], n => n * n);
```

ou mieux utiliser [les fonctions natives d'ES6](https://github.com/you-dont-need/You-Dont-Need-Lodash-Underscore)

```js
[4, 8].map(value => value * value);
```

Points de contrôle

- [ ] Vérifiez que vous n'importez jamais globalement la librairie `lodash`
- [ ] Vérifiez que vous n'avez pas la librairie `lodash` dans votre package.json (mais plutôt les sous modules).

## Liens

- [Documentation Officielle de Lodash](https://lodash.com/)
- [Comment se passer d'underscore et Lodash + avoir les regles ESLint pour proposer une alternative ES6](https://github.com/you-dont-need/You-Dont-Need-Lodash-Underscore)
