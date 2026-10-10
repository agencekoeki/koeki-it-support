# Contributing

Thank you for considering it. koeki-it-support v0.1 was built from books, papers and Microsoft documentation. What it lacks is the part of the job that never makes it into books: what a seasoned technician notices in the first two minutes, and when they drop a lead.

[En français plus bas](#en-français).

## What we need most: real cases from field technicians

If you fix Windows PCs for a living (or have for years), the most valuable thing you can give is **a real case you handled**, told in a specific format. Research on expert knowledge shows that experts can't fully describe how they work in general, but they can recount a specific case in rich detail. So please don't write "how I troubleshoot slow PCs". Tell us about one PC.

### The case format

Every case pattern in the skill follows the same four parts. Please use them:

| Part | Question to answer | Example |
|---|---|---|
| **Cues** | What did you see, hear or measure that caught your attention? | "Same 30-second freeze at every logon, whatever the load." |
| **Likely story** | What did you think was going on, and why? | "Something waiting for a timeout: a network drive or a dead DNS server." |
| **First move** | What did you check or do first, and why that before anything else? | "Asked what was mapped; tested name resolution against each DNS server." |
| **Signal to abandon the track** | What would have made you drop this lead and look elsewhere? | "If the delay varied a lot from one logon to the next: that's load, not a timeout." |

Then, if you can, add:

- **Context:** Windows version, type of machine, age, hard drive or SSD.
- **What the person said** at first, in their words.
- **What fooled you, or could have:** a misleading indicator, a red herring, a tool that lied.
- **How you confirmed the fix:** what you measured, and after what kind of restart.
- **What a beginner would have done wrong.**

### Anonymize everything

No names of people or companies, no IP addresses, no serial numbers, no license keys, no screenshots showing personal data. Change any detail that could identify a client. Brands of software are fine when they matter to the diagnosis.

### How to submit a case

Open an issue titled `Case: <short description>` and paste the format above. You can also send a pull request that adds your case to the evaluation scenarios in [evals/scenarios.md](evals/scenarios.md). We will discuss with you how it should change the skill.

## Changes to SKILL.md

Every change to [koeki-it-support/SKILL.md](koeki-it-support/SKILL.md) goes through an issue or a pull request, and is reviewed before it is merged. No direct pushes, including from maintainers.

A good pull request on the skill:

- explains which behaviour it changes, and why;
- cites a source for any factual claim about Windows (Microsoft documentation first), or describes the real case it comes from;
- says which scenarios in [evals/scenarios.md](evals/scenarios.md) it affects, and adds one if none covers the change;
- keeps the safety model intact: consent per action, a restore point before the first change, one change at a time, a journal;
- keeps SKILL.md under 500 lines, as the [Agent Skills specification](https://agentskills.io/specification) recommends.

## Other welcome contributions

- **Corrections**, with a source: an outdated menu path, a wrong event ID, a command that fails on a localized Windows.
- **New evaluation scenarios**, especially from incidents with several stacked causes.
- **Scored evaluation runs**, using [evals/rubric.md](evals/rubric.md), with the transcript.
- **Better wording** for non-technical people, in any language.

## What we won't accept

- Scripts or commands that change the system without going through the consent levels.
- Registry cleaners, "optimizers", third-party driver updaters, debloat scripts or tweak packs, even as optional extras.
- Anything that turns off Windows Update, Microsoft Defender, the firewall or UAC.
- Claims about performance or carbon that no source supports.

## License

By contributing, you agree that your contribution is released under the [MIT license](LICENSE) of this project.

---

## En français

Merci de vous y intéresser. La v0.1 de koeki-it-support a été construite à partir de livres, d'articles et de la documentation de Microsoft. Il lui manque ce que les livres ne disent pas : ce qu'un technicien expérimenté remarque dans les deux premières minutes, et le moment où il abandonne une piste.

### Ce qui nous aide le plus : de vrais cas racontés par des techniciens

Si vous dépannez des PC Windows au quotidien, le plus précieux est de nous raconter **un vrai cas que vous avez traité**. Les recherches sur le savoir des experts le montrent : on n'arrive pas à décrire sa méthode en général, mais on se souvient très bien d'un cas précis. Ne nous écrivez donc pas « comment je dépanne un PC lent ». Racontez-nous un PC.

Chaque cas suit le format des cas types du skill :

| Partie | La question | Exemple |
|---|---|---|
| **Indices** | Qu'avez-vous vu, entendu ou mesuré qui vous a mis la puce à l'oreille ? | « Le même gel de 30 secondes à chaque ouverture de session, quelle que soit la charge. » |
| **Histoire probable** | Que pensiez-vous qu'il se passait, et pourquoi ? | « Quelque chose qui attend une expiration : un lecteur réseau ou un DNS muet. » |
| **Premier geste** | Qu'avez-vous vérifié ou fait en premier, et pourquoi avant tout le reste ? | « J'ai demandé ce qui était connecté en réseau ; j'ai testé la résolution de noms sur chaque serveur DNS. » |
| **Signal pour abandonner la piste** | Qu'est-ce qui vous aurait fait lâcher cette piste pour chercher ailleurs ? | « Si le délai avait beaucoup varié d'une session à l'autre : c'est de la charge, pas une expiration. » |

Ajoutez si possible : le contexte (version de Windows, type et âge de la machine, disque dur ou SSD), les premiers mots de la personne, ce qui vous a trompé ou aurait pu le faire, comment vous avez confirmé la réparation, et l'erreur qu'aurait faite un débutant.

**Anonymisez tout** : aucun nom de personne ni d'entreprise, aucune adresse IP, aucun numéro de série, aucune clé de licence, aucune capture d'écran avec des données personnelles. Les marques de logiciels sont bienvenues quand elles comptent pour le diagnostic.

**Pour proposer un cas**, ouvrez une issue intitulée `Case: <description courte>` (en français si vous préférez) et suivez le format ci-dessus.

### Modifier le SKILL.md

Toute modification de [koeki-it-support/SKILL.md](koeki-it-support/SKILL.md) passe par une issue ou une pull request, relue avant fusion. Aucun envoi direct, mainteneurs compris. Une bonne pull request explique le comportement qu'elle change et pourquoi, cite une source (la documentation de Microsoft d'abord) ou le cas réel dont elle vient, indique les scénarios d'évaluation concernés, et garde intact le modèle de sécurité : accord action par action, point de restauration avant le premier changement, un changement à la fois, un journal.

En contribuant, vous acceptez que votre contribution soit publiée sous la [licence MIT](LICENSE) du projet.
