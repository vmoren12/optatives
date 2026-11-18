# Apptatives

**Aplicatiu web per assignar optatives a l’alumnat** a partir de les seves preferències, les places de cada matèria i els criteris del centre.

👉 **Fes-lo servir aquí: <https://vmoren12.github.io/optatives/>**

Funciona del tot al navegador: no cal instal·lar res ni crear cap compte, i **les dades de l’alumnat no s’envien enlloc**.

## Què fa

L’aplicatiu guia el procés en set passos:

1. **Dades**: carrega un Excel (`.xlsx`, `.xls`, `.ods`, `.csv`…) amb una fila per alumne i les matèries triades per ordre de preferència (fins a 8). Opcionalment: grup, escoleta, gènere, nivell i columnes per ajuntar o separar alumnes.
2. **Revisió**: detecta problemes al fitxer (noms de matèria semblants, valors poc freqüents, places insuficients…) i en proposa correccions.
3. **Matèries**: places, mínims, trimestres en què s’ofereix cada matèria i quantes assignacions rep cada alumne.
4. **Ajuntar i separar**: grups d’alumnes que han de coincidir (o no) a la mateixa optativa, de manera obligatòria o preferent.
5. **Criteris**: què pesa més quan no hi ha places per a tothom a la primera tria.
6. **Assignació**: calcula una proposta i permet ajustar-la a mà arrossegant alumnes, fixar-los i recalcular.
7. **Resultats**: estadístiques i exportació a Excel.

Si no tens dades a mà, pots provar-lo amb l’**exemple** integrat o descarregar-ne la **plantilla**.

## Privadesa

- Els fitxers es llegeixen localment al navegador; no hi ha cap servidor que els rebi.
- La feina es desa automàticament al `localStorage` del navegador. Per conservar-la o moure-la a un altre ordinador, fes servir **Desar projecte** (fitxer `.json`) i **Obrir**.
- L’únic contingut extern que es carrega són les tipografies (Google Fonts) i la llibreria [SheetJS](https://sheetjs.com/) per llegir i escriure Excel (cdnjs, amb verificació d’integritat SRI).

## Ús local

És un únic fitxer HTML autocontingut. Pots:

- Obrir `index.html` directament amb el navegador, o
- Servir la carpeta amb qualsevol servidor estàtic, per exemple:

  ```sh
  python -m http.server 8000
  # i obre http://localhost:8000
  ```

Per llegir Excel cal connexió a internet la primera vegada (per carregar SheetJS).

## Estructura del repositori

```
index.html     L’aplicatiu complet (HTML, CSS i JavaScript)
CHANGELOG.md   Historial de versions
LICENSE        Llicència MIT del codi
.nojekyll      Desactiva el processament Jekyll a GitHub Pages
```

## Publicació

La pàgina es publica amb **GitHub Pages** des de la branca `main` (carpeta arrel). Cada push a `main` actualitza <https://vmoren12.github.io/optatives/>.

Per publicar una versió nova:

1. Actualitza `APP_VERSION` a `index.html` i el número del peu de pàgina.
2. Afegeix l’entrada corresponent a [`CHANGELOG.md`](CHANGELOG.md).
3. Fes commit, crea l’etiqueta (`git tag v1.x.y`) i fes push amb `--tags`.

## Llicència

© 2026 Víctor Moreno de la Torre · Psicòleg i orientador educatiu

- **Codi**: [MIT](LICENSE)
- **Continguts** (textos i documentació): [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.ca)
