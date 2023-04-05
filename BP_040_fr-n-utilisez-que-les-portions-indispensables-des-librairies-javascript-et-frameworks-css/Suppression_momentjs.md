# Remplacement de momentjs par datefns(BP040)

## Règle

:recycle: [MomentJs](https://momentjs.com/) est une librairie non maintenue qui inclut, de base, l'ensemble des configurations globales du monde, ce qui a un impact conséquent sur la taille des ressources statiques.

## Gains

Optimisation de la taille des ressources statiques.

## Valider la mise en place de la bonne pratique

:x: Code à éviter

```js
import moment from "moment";
const age = moment().diff(birthday, "years");
```

:heavy_check_mark: Code à favoriser

```js
import differenceInYears from "date-fns/differenceInYears";

const age = differenceInYears(new Date(), birthday);
```

Points de contrôle

- [ ] Vérifier que la dépendance n'est plus dans le package.json
- [ ] Vérifier qu'il n'y ait plus d'import de MomentJs
- [ ] Vérifier qu'il n'est plus dans le bundle généré
- [ ] Vérifier que vous utilisez, à minima, la [version 2.0 du toolkit Axa](https://github.com/AxaGuilDEv/react-toolkit/blob/master/MIGRATION.md#date-input)

## Liens

- [Remplacer MomentJs](https://artemdemo.com/blog/20181104-replacing-momentjs/)
