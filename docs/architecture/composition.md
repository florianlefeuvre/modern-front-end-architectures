# Composition

La plupart des **frameworks front-end modernes** proposent d'architecturer vos applications par **composition**, un design pattern particulièrement adapté à l'écosystème fonctionnel de JavaScript.

> *Intégrer un schéma relationel entre composants*

Architecturer par composition permet - à contrario de l'héritage - d'obtenir des briques de composants pures avec système d'Input/Output respectant plus facilement le **SRP**.

> *Intégrer un schéma d'un composant avec I/O*

Les balises HTML de vos vues mais aussi la logique de vos controllers étant encapsulés dans un composant, on évite la duplication de code d'un point de vue interface.

> *Intégrer une animation de transformation de balises html vers un composant*

En revanche, la composition ne permet pas toujours de respecter le **DRY** notamment lorsqu'il est question de logique métier. En effet, vos composants deviendront naturellement plus complexes avec le temps puisqu'ils risquent d'encapsuler de la logique métier lié au fonctionnel, mais aussi de la gestion d'état local et parfois une nécessité d'interraction avec des états de plus haut niveau.

Différents design patterns vont permettre d'atténuer cet effet, notamment :
 - [Container/Presentational pattern](../patterns/container-presentational.md)
 - Providers pattern
 - Hooks pattern

## Résumé

- ✅ Des briques hautements modulables et réutilisables
- ✅ Une compréhension du scope simplifiée pour les devs juniors
- ✅ Un niveau de couplage faible
  - Pas de chaîne d'héritage à maintenir et moins d'effets de bords
  - Apporte une flexibilité accrue lorsqu'il est question de répondre à de nouveaux besoins fonctionnels
- ✅ Meilleure collaboration avec les designers
  - Leurs designs d'interfaces fonctionnant aussi par composition
- ✅ Une communication plus facile entre les composants proches
  - Notamment lorsqu'ils sont en relation directe (parent/enfant)
- ❌ Une communication plus fastidieuse entre les composants éloignés
  - Notamment lorsque ces derniers sont séparés par plus d'un seul niveau de parenté
- ❌ Peut provoquer de la répétition de code inutile sur les briques de logique métier