# Projet 4 — Application .NET HomeSkolar — Livrables

**Formation :** Développeur d'application back-end .NET (OpenClassrooms)
**Projet :** Désignez une application .NET adaptée aux besoins d'un client
**Client :** HomeSkolar (association) — **Prestataire :** CodeIguanas (Entité Web)
**Date :** 2026

---

## 1. Contenu des livrables

| Fichier | Description |
|---|---|
| **`01_Cahier_des_charges.pdf`** | Cahier des charges complet : spécifications fonctionnelles, veille technologique, spécifications techniques et diagramme de classes UML. |
|
| **`02_Backlog_Produit.pdf`** | Backlog produit : 25 user stories priorisées (MoSCoW), critères d'acceptation *Given-When-Then*, dépendances, estimations et plan de 4 sprints. |
|
| **`03_Support_presentation.pdf`** | Support de présentation (12 slides, ≤ 15 min) : contexte, fonctionnalités, choix techniques. |
| `03_Support_presentation.pptx` | Même présentation, **version PowerPoint éditable**. |
|
| **`LIEN_PUBLIC_Backlog.md`** | Emplacement du lien public Notion 


---

## 2. Correspondance avec les attendus du projet

### Cahier des charges
- **Spécifications fonctionnelles** — 4 fonctionnalités majeures (Comptes & mise en relation,
  Messagerie, Rencontres/Calendrier, Tâches), découpées en sous-fonctionnalités, chacune
  reliée à un besoin client (table de traçabilité). Couvre les minima exigés : connexion,
  inscription, communication élève/tuteur, configuration des rencontres, planification des tâches.
- **Veille technologique** — 3 sources variées et pertinentes (Microsoft Learn, Stack Overflow
  Survey, DB-Engines Ranking), justification de la sélection et de l'enjeu.
- **Spécifications techniques** — architecture + choix de chaque technologie (rôle + justification
  vs alternatives), sécurité/RGPD, réponse aux besoins.
- **Diagramme de classes UML** — 9 classes métier + 6 énumérations, héritage et associations
  avec multiplicités, conçu pour être extensible.

### Backlog produit
- ≥ 1 user story par fonctionnalité majeure, format
  *« En tant que … je veux … afin de … »*.
- ≥ 1 critère d'acceptation par user story, au format *Étant donné – Quand – Alors*.
- Priorisation MoSCoW, dépendances explicites, estimation en jours-homme tenant compte de
  l'équipe (2 back-end + 2 front-end), plan de livraison en 4 sprints.

### Support de présentation
- ≥ 1 slide pour : le contexte, les fonctionnalités, les choix techniques.
- Fonctionnalités additionnelles **proposées séparément** (slide « Évolutions possibles »),
  hors spécifications fonctionnelles.

---

## 3. Choix techniques retenus (résumé)

| Couche | Technologie | Rôle |
|---|---|---|
| Front-end | **Blazor WebAssembly (C#)**, Radzen Blazor (Scheduler) | Interface élève / tuteur / admin, calendrier |
| Back-end | **ASP.NET Core (.NET 10 LTS)**, C# | API REST, logique métier |
| Temps réel | **SignalR** | Messagerie & notifications |
| Sécurité | **ASP.NET Core Identity + JWT** | Authentification, mot_de_passe haché |
| Données | **Entity Framework Core 10** + **Microsoft SQL Server** | Accès aux données, base relationnelle |
