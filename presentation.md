---
marp: true
theme: uncover
_class: invert
---

# 30g eqCO2

is the estimation of the CO2 emissions of solar photovoltaic energy, for the production of 1 kWh of electricity, according to the French Environment and Energy Management Agency (ADEME).

According to the GIEC,
* the energy emitting the fewest CO2 are nuclear power and onshore wind: 11-12 g eqCO2/kWH
* and most emitting is coal: 820 g eqCO2/kWH

---

# :recycle: Rule

Our rules focus on the Javascript frontend.
The objective is to fight against software obesity.
3 rules focus on the matter of software dependency obsolescence, by reducing the size of the dependencies used, and avoid using non maintained dependencies.

How to do without Lodash Underscore: https://github.com/green-code-initiative/ecoCode-challenge/issues/35
How to do without MomentJS: https://github.com/green-code-initiative/ecoCode-challenge/issues/37
How to identify packages with security flaws: https://github.com/green-code-initiative/ecoCode-challenge/issues/52


3 other rules about package size reduction: 
- optimize browserlist tag in package.json : https://github.com/green-code-initiative/ecoCode-challenge/issues/54
- utiliser l'élement picture plutot qu'img pour utiliser les nouveaux formats de compression :
  https://github.com/green-code-initiative/ecoCode-challenge/issues/53
- utiliser le lazy loading pour ne pas charger les images / iframes qui ne sont pas affichés : https://github.com/green-code-initiative/ecoCode-challenge/issues/34
