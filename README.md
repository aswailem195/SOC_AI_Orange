# SOC AI Orange - VET

Projet académique collectif réalisé en Master 2 Cybersécurité, en
collaboration avec Orange, de novembre 2025 à mars 2026.

VET (Vulnerable Exploitation Tool) explore l'utilisation d'un assistant IA
pour aider un analyste SOC à distinguer les vulnérabilités réellement
prioritaires des vulnérabilités seulement théoriques.

## Objectif

Le prototype combine plusieurs sources et méthodes de priorisation :

- CVSS pour mesurer la sévérité technique ;
- EPSS pour estimer la probabilité d'exploitation ;
- CISA KEV pour identifier les vulnérabilités exploitées ;
- corrélation avec les journaux de sécurité ;
- règles VMC et modèle XGBoost pour la priorisation ;
- pipeline RAG et LLM local pour produire une analyse contextualisée.

L'objectif est de fournir à l'analyste une réponse explicable, accompagnée
d'éléments factuels et d'une proposition de traitement.

## Architecture étudiée

Le rapport décrit notamment :

- une interface Streamlit ;
- un agent d'orchestration `SecurityAssistant` ;
- une recherche hybride SQLite et FAISS ;
- un analyseur de journaux ;
- une génération structurée en deux passes ;
- un laboratoire Docker volontairement vulnérable pour les essais.

Le laboratoire est un environnement pédagogique isolé. Il ne doit jamais être
déployé sur un système de production ou exposé sans mesures de confinement.

## Documents

- [Présentation du projet](docs/presentation-soc-ai-orange.pdf)
- [Rapport technique compilé](report/soc-ai-orange-report.pdf)
- [Source LaTeX du rapport](report/main.tex)
- [Bibliographie](report/biblioFile.bib)

## Organisation du dépôt

```text
.
|-- docs/
|   `-- presentation-soc-ai-orange.pdf
|-- report/
|   |-- img/
|   |-- biblioFile.bib
|   |-- llncs.cls
|   |-- main.tex
|   |-- malware.png
|   |-- reachability.pdf
|   |-- soc-ai-orange-report.pdf
|   `-- splncs04.bst
`-- README.md
```

## Compilation du rapport

Depuis le dossier `report` :

```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

## Auteurs

- Masha Mirza Zad Ziabary
- Abdullah Ahmed-Bark Swailem
- Mirwis Satarzai
- Damien Maris

## Périmètre

Ce dépôt documente un projet académique collectif. Il contient les livrables
de présentation et de recherche fournis pour le portfolio, mais pas le code
complet ni les données du prototype.

