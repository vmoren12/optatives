# Historial de canvis

El format segueix [Keep a Changelog](https://keepachangelog.com/ca/1.1.0/) i el projecte usa [versions semàntiques](https://semver.org/lang/ca/).

## [1.4.0] - 2026-11-18

### Canviat
- L’aplicatiu passa a dir-se **Apptatives** (títol, capçalera i metadades).
- La clau de desat al navegador passa a ser `apptatives.projecte.v1`. La feina desada amb la clau antiga (`optatives.projecte.v1`) es migra automàticament en obrir l’aplicatiu.
- Els projectes desats s’identifiquen amb `app: "apptatives"`. Els fitxers de projecte antics es continuen obrint sense canvis.
- El nom per defecte dels fitxers exportats és `apptatives-…` quan el procés no té nom.

### Afegit
- Metadades de descripció, Open Graph i color de tema.
- Verificació d’integritat (SRI) de la llibreria SheetJS carregada des de cdnjs.
- Missatge per a navegadors sense JavaScript.
- Publicació a GitHub Pages: <https://vmoren12.github.io/optatives/>.

## [1.3.0]

- Versió inicial publicada al repositori.

[1.4.0]: https://github.com/vmoren12/optatives/releases/tag/v1.4.0
