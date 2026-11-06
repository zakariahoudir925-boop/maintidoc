# MAINTiDOC

Assistant documentaire multimodal et agentique pour la maintenance industrielle.

**Module :** IA générative multimodale — EMSI 2026
**Équipe :** Zakaria Houdir, Anas Essadeq (`ESSADEQ-HOUDIR`)
**État :** livrable 1 terminé — cadrage, corpus documentaire, architecture cible.

## Contenu du dépôt

| Dossier | Contenu |
|---|---|
| `corpus/documents/famille_1/` | 25 PDF — pompes centrifuges PX-250-H (`POMPE-A-01`) |
| `corpus/documents/famille_2/` | 24 PDF — compresseurs à vis AC-90 (`COMP-B-02`) |
| `corpus/images/` | 10 figures exportées, 3 pages scannées, 1 photographie de panneau |
| `corpus/inventaire.csv` | registre du corpus : 50 lignes, 20 colonnes |
| `corpus/prompts_corpus.md` | prompts P01 à P11, journal des corrections, analyse critique |
| `docs/diagrammes/` | sources des figures du rapport (Mermaid et PNG) |

## Le corpus

Cinquante éléments, deux familles d'équipements, sept types de documents. Le corpus est
entièrement synthétique : les documents ont été rédigés par l'équipe avec l'assistance d'un
modèle de langage, puis relus et corrigés. Les constructeurs sont fictifs et chaque document
porte un avertissement en ce sens. Aucune donnée personnelle réelle n'est utilisée.

Cas de test prévus pour l'évaluation : deux paires contradictoires (4 documents), deux documents
piégés contenant une tentative d'injection de prompt, trois cas ambigus, trois documents scannés
sans couche texte. Ces cas sont signalés dans la colonne `usage_test` de l'inventaire.

## Livrable 1

Le rapport (parties 2.1 à 2.6, 12 pages hors annexes) accompagne ce dépôt. Il fixe :

1. le cadrage : utilisateurs, cas d'usage, objectifs vérifiables, périmètre et hors-périmètre ;
2. le corpus : 50 éléments, inventaire, traçabilité des prompts ;
3. l'architecture cible : blocs, points de contrôle, parcours d'une requête ;
4. les flux de données : ingestion, requête, création de ticket, métadonnées, modèle d'accès ;
5. l'analyse de douze risques ;
6. le planning des semaines 2 à 6 et la répartition des rôles.

## Précautions

- Les valeurs techniques du corpus sont fictives ou simplifiées : aucune ne doit servir de
  référence pour une intervention réelle.
- Les deux documents piégés (`guide_optimisation_pompe_piegee`, `note_service_comp_piegee`)
  contiennent une instruction malveillante volontaire, destinée aux tests de la semaine 5.
- Aucun secret, aucune clé d'API, aucun fichier d'environnement ne doit entrer dans ce dépôt.
