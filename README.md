# Agente de trading cuantitativo

Repositorio: [Gfrati97/Agente-trading-cuantitativo](https://github.com/Gfrati97/Agente-trading-cuantitativo).

Proyecto sobre **SOLUSDT**, con velas de **5 minutos** y un modelo **V2 de clasificación**: `0 = NO OPERAR`, `1 = LONG`, `2 = SHORT`.

## Estructura

```text
notebooks/agente_trading_cuantitativo.ipynb  Notebook principal
src/                                      Código del proyecto (reservado)
data/                                     Datos locales, fuera de Git
models/                                   Artefactos de modelos locales
reports/                                  Informes y resultados
```

El notebook principal procede de `agente_trading_cuantitativo_ordenado.ipynb`: solo se cambió su ubicación y nombre; se conservaron todas sus celdas, metadatos y salidas. Esta preparación no incorpora estrategias ni cambios en la lógica del modelo.

## OOS congelado

El conjunto fuera de muestra (OOS) debe permanecer congelado y reservado para la evaluación final. **No se debe utilizar para ajustar modelos, filtros ni parámetros**, ni para seleccionar estrategias. Los diagnósticos y decisiones de ajuste deben limitarse a los conjuntos de entrenamiento y validación correspondientes.

El notebook conserva secciones históricas, incluidas pruebas OOS previas, fuera del pipeline V2 activo. No ejecutar indiscriminadamente todas las celdas ni reutilizar esos resultados históricos para ajustar el modelo. El notebook no se ejecutó durante esta organización.

## Datos y modelos

- `data/` excluye por defecto todos sus archivos, salvo `.gitkeep`, para evitar versionar CSV, Parquet o datasets pesados, independientemente del formato.
- `models/` excluye archivos `.pkl`, `.pickle` y `.joblib`, incluidos los comprimidos.
- Los CSV y Parquet también se ignoran fuera de `data/` para evitar incorporarlos accidentalmente desde el directorio de trabajo del notebook.
- No se incluyen datos ni modelos entrenados en esta preparación.

El notebook conserva sus rutas originales: espera `SOLUSDT_5m_futures.csv` en el directorio de trabajo. Trasladar el notebook no adapta esas rutas automáticamente. Para mantener los datos en `data/` sin modificar la lógica, usar esa carpeta como directorio de trabajo del kernel cuando corresponda. No se verificó la ejecución ni se definieron nuevas dependencias en esta tarea.
