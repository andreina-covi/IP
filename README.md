# IP

Presentaciones Beamer (Introducción a la Programación).

## Estructura

```
IP/
├── beamerthemefibeamer.sty
├── fibeamer/                 # tema (colores, tipografía, logos)
├── resources/                # imágenes compartidas
├── slides/
│   ├── beamerthemefibeamer.sty -> ../beamerthemefibeamer.sty
│   ├── algoritmo.tex
│   └── ped-pdflatex.tex
└── latexmkrc
```

## Compilar

Abre un `.tex` en `slides/` y compila desde ahí, o:

```bash
latexmk -pdf -cd slides/algoritmo.tex
latexmk -pdf -cd slides/ped-pdflatex.tex
```

## Añadir otra presentación

1. Crea el `.tex` en `slides/`.
2. Cabecera:

```latex
\usetheme[faculty=ped,basePath=../fibeamer,logo=../fibeamer/logo/mu/Logo-UC-3.png]{fibeamer}
\graphicspath{{../resources/}}
```

3. Imágenes solo por nombre; el archivo va en `resources/`:

```latex
\includegraphics[width=0.5\linewidth]{mi-imagen.png}
```
