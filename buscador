#!/bin/bash
# Busca la palabra "home" en los archivos de una carpeta

PALABRA="home"
CARPETA="${1:-.}"

if [ ! -d "$CARPETA" ]; then
    echo "Error: la carpeta $CARPETA no existe"
    exit 1
fi

grep -rl "$PALABRA" "$CARPETA"
