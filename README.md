# Reporte de Incidencias - Examen de Fotogrametría (WebODM)

- **Estudiante:** José Antonio Anduray Bonilla
- **Número de cuenta:** 20181004327
- **Herramienta:** WebODM sobre Máquina Virtual Ubuntu (Hyper-V)

## Descripción del Problema e Incidencia Técnica
Durante el procesamiento del conjunto de datos de 40 imágenes para el proyecto `Examen_1`, el sistema experimentó fallos críticos e interrupciones abruptas provocadas por el kernel de Linux (señal `SIGKILL` / *OOM Killer*). 

### Justificación:
1. **Restricción de Recursos:** El entorno local de pruebas en Hyper-V se vio limitado estrictamente a 2 GB de memoria RAM debido a la capacidad máxima disponible en el sistema anfitrión.
2. **Consumo de Memoria:** Las etapas avanzadas de fotogrametría (específicamente la generación masiva de mapas de profundidad y ortomosaicos densos) superaron el umbral de los 2 GB, colapsando los contenedores de procesamiento.
3. **Evidencia Adjunta:** En la carpeta `Evidencias_Examen` se encuentran las capturas de pantalla de la terminal que registran el corte por falta de memoria y el estado del nodo al momento de la incidencia.
