# Control de staffing

Aplicació web d'una sola pàgina per controlar el staffing a partir d'un fitxer Excel. No requereix instal·lació ni servidor: tot es processa al navegador i les dades no surten del dispositiu.

## Funcionalitats

- Càrrega d'un fitxer `.xlsx` o `.xlsm` (arrossegant-lo o seleccionant-lo).
- Tres vistes:
  - **Assignacions:** demandes T&M en estat `ASIGNADO` que vencen dins del període.
  - **Valoració CXB:** demandes T&M en estat `VALORACION CXB`, amb gràfics per manager i per mes.
  - **Projectes:** projectes actius que vencen dins del període.
- Filtres per cerca, manager i termini (vence avui, queden dies, vençudes).
- Opció per incloure assignacions ja vençudes.
- Gràfics de barres i de cercle (Chart.js).
- Exportació de les tres vistes a un nou Excel.

## Format del fitxer d'entrada

El fitxer ha de contenir dues pestanyes amb aquests noms exactes:

| Pestanya | Columnes necessàries |
|---|---|
| `Detalle T&M` | `Estado`, `Fecha Fin`, `T&M / Proyecto` (i les columnes que vulguis veure) |
| `Detalle proyectos asignados` | Columnes de projectes |

Aquest repositori **no inclou dades reals**. Utilitza el teu propi fitxer de staffing.

## Ús

Opció 1, obrir localment: descarrega el repositori i obre `index.html` al navegador.

Opció 2, GitHub Pages: a *Settings → Pages*, selecciona la branca `main` i la carpeta `/ (root)`. L'aplicació quedarà disponible a `https://<usuari>.github.io/<repositori>/`.

## Tecnologia

- HTML, CSS i JavaScript en un sol fitxer (`index.html`).
- [SheetJS (xlsx) 0.18.5](https://cdnjs.com/libraries/xlsx) per llegir i escriure Excel.
- [Chart.js 4.4.1](https://cdnjs.com/libraries/Chart.js) per als gràfics.

Les biblioteques es carreguen des de cdnjs, així que cal connexió a internet.

## Llicència

Pendent de definir.
