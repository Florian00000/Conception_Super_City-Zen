# Conception_Super_City-Zen

[lien figma de la mquette](https://www.figma.com/design/rVyKMxsxSqqOWMXrdTnmxM/Wireframe-%26-Maquette?node-id=0-1&t=9l2QNuBRIwKBBTY4-1)

## Définition des entités du dervice **Hübert City-zen!!** ;)

### User
- Un user peut avoir plusieurs rôles (cumulatif): citoyen, admin, municipalitée.
- Un citoyen peut proposer des idées (comme un topic sur un forum).
- Un citoyen peut commenter sur un sujet (entité Discussion), il peut aussi répondre à un commentaire
- Un citoyen ne peut voter qu'une fois par projet.
- Municipalitée peut crée un projet ou transformer une idée en projet.
- admin gère la modération des discussions et des idées.
- admin créer les users.
- municipalité et admin peuvent gérer le CRUD des catégories

### Identifier
- Un user est lié à un identifier
- Les identifiers sont crée en amont de l'user
- le champ login de identifier est unique, et fournis à un citoyen pourqu 'il puisse s'inscrire. Il sert également d'username.
- le champ is_used est un boolean qui indique si un identifier a déjà été utilisé pour créer un compte.

### Idée
Une idée est comme un topic de forum.
- Une idée est soumise par les citoyens.
- Les citoyens peuvent répondre à une idée à travers l'entitée Discussion.
- Une idée peut être transformé en Poject par un membre de la municipalitée.
- Les citoyens peuvent *upvote* pour une idée (fonctionne avec l'entitée vote), pour mettre en avant cette idée auprès de la municipalitée.
### Discussion
Une discussion est un message de réponse.
- Un citoyen peut répondre à une idée (idea).
- Un citoyen peut répondre à un message (discussion).
### Projet
Un projet est une entitée créer par la municipalitée pour être soumise à un vote.
- Municipalitée peut créer un projet.
- Municipalitée peut transformer l'idée d'un citoyen en projet.
- Un projet est soumis à un vote jusqu'à une date de cloture (votation_close_at)
### Vote
- Un vote est lié à un projet.
- is_yes est un booléen qui définit si le citoyen à voté pour ou contre.
- Un vote est lié à un citoyen et chaque citoyen ne peut voter qu'une fois par projet.
- La municipalitée peut voir la somme totale des votes pour ou contre mais ne peut pas voir l'id du citoyen qui à voté.
