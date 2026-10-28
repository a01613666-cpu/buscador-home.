#!/bin/bash
# Busca la palabra "home" en los archivos de una carpeta
# Uso: bash buscar.sh [carpeta]

PALABRA="home"
CARPETA="${1:-.}"

if [ ! -d "$CARPETA" ]; then
    echo "Error: la carpeta $CARPETA no existe"
    exit 1
fi

RESULTADOS=$(grep -rIl "$PALABRA" "$CARPETA" 2>/dev/null)

if [ -z "$RESULTADOS" ]; then
    echo "No se encontro la palabra '$PALABRA' en $CARPETA"
else
    echo "Archivos que contienen la palabra '$PALABRA':"
    echo "$RESULTADOS"
    echo "Total de archivos: $(echo "$RESULTADOS" | wc -l)"
fi
