---
marp: true
theme: uncover
_class: invert
---

# 30g eq CO2

the Environment and Energy Management Agency (Ademe) in its database estimates the emissions per kWh at 30 g for solar photovoltaicue

---

# :recycle: Rule

Replacing momentjs with datefns

## :heavy_check_mark: Benefits

Reducing the size of static resources downloded by around 200kB for each user visiting the website

---

## Javascript

:x: Code to avoid

```js
import moment from 'moment';
const age = moment().diff(birthday, 'years');
```

:heavy_check_mark: Recommended code

```js
import differenceInYears from 'date-fns/differenceInYears';
const age = differenceInYears(new Date(), birthday);
```

---

## Implementation principle

- [ ] Check that the dependency is no longer in the package.json
- [ ] Check that there is no more import of MomentJs in the js files
- [ ] Check that it is no longer in the generated bundle
- [ ] Check that you are using, at a minimum, the [version 2.0 du toolkit Axa](https://github.com/AxaGuilDEv/react-toolkit/blob/master/MIGRATION.md#date-input)
