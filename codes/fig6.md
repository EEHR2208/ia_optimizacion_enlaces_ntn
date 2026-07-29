¡Entendido! Asumo el rol de **Experto en Visualización de Datos Científicos y Arquitecturas Aeroespaciales**. Procedo a aplicar el protocolo de validación técnica antes de cualquier generación.

---

## FASE 1: Mapeo de Entidades (Análisis del Contexto LaTeX)

* **Entidad Core bajo análisis:** Rendimiento de interferencia y calidad de señal en una red no terrestre (NTN) 6G con 6 satélites LEO y hasta 200 usuarios.
* **Métrica Clave:** Función de Distribución Acumulada (CDF) de la Relación Señal a Interferencia más Ruido (SINR).
* **Nivel de Abstracción:** Datos cuantitativos de simulación y curvas de probabilidad empírica.
* **Relaciones Críticas:** * El esquema propuesto (`LAM-DRL`) desplaza la CDF hacia la derecha (valores de SINR superiores).
* Reducción marcada en la cola inferior (menos usuarios experimentando baja SINR / menor probabilidad de *outage*).
* Superación explícita sobre los baselines: DRL Estándar (`DDPG`/`DQN`), Heurísticas (`PF`), y el estado del arte de referencia (Park et al.).



---

## FASE 2: Auditoría y Reporte de Hallazgos Críticos

### 1. Contraste de Coherencia

El prompt base captura adecuadamente la naturaleza matemática de la `fig6.png` (una gráfica CDF de SINR). Sin embargo, falla críticamente en las restricciones de formato (texto incrustado) y en la precisión de las etiquetas de los baselines según la nomenclatura del texto científico.

### 2. LISTA DE DISCREPANCIAS (Explícita)

* **Falta de Texto Explicativo/Incrustado:** El prompt base solicita *"sin texto incrustado"*. Esto viola el estándar de publicación IEEE y tu requerimiento de control de estilo. Una gráfica científica *debe* tener etiquetas de ejes ($X$ e $Y$), unidades ($dB$) y una leyenda legible.
* **Nomenclatura Inexacta de Baselines:** * El prompt base menciona "Heuristic". El texto científico especifica que es una heurística proporcional a la demanda (`PF`).
* El prompt base menciona "DRL Standard". El texto especifica `DDPG`/`DQN` estándar.
* El prompt base dice "Proposed". El texto define formalmente el framework como `LAM-DRL` (o enfoque guiado por LAM).


* **Detalle del Comportamiento Físico:** Para reflejar la "reducción de la cola inferior" mencionada en el texto, la curva de `LAM-DRL` debe comenzar sustancialmente más a la derecha en el eje X en comparación con los baselines, mostrando que casi ningún usuario sufre de SINR crítica (coincidiendo con el *outage* < 3% de la Tabla 3).

### 3. Control de Estilo

* **Formato:** Estándar IEEE, vector 2D, plano, limpio.
* **Paleta:** Azul Cobalto (`#0047AB`) para la solución propuesta, Gris Técnico (`#4A4A4A`) para el baseline principal, Negro y variantes punteadas/guionadas para los baselines secundarios.
* **Texto:** Se **incluirán** etiquetas vectoriales nítidas para los ejes y la leyenda.

---

## FASE 3: Explicación y Justificación de Pre-ejecución

### 1. Disposición Espacial y Elementos

* **Ejes Cartesianos:** Eje X horizontal etiquetado como `SINR (dB)` con ticks de -10 a 30. Eje Y vertical etiquetado como `CDF` con ticks de 0.0 a 1.0.
* **Curvas (De izquierda a derecha, peor a mejor rendimiento):**
1. `Heuristic (PF)`: Curva más a la izquierda, indicando peor SINR general.
2. `Park et al. [23] (DQN)`: Curva intermedia.
3. `DRL Standard (DDPG)`: Curva intermedia-alta.
4. `Proposed LAM-DRL`: Curva ubicada en el extremo derecho, con una subida pronunciada que arranca cerca de los 5-10 dB (evitando la zona de -10 dB, lo que demuestra la mitigación de la cola inferior de interferencia).


* **Cuadrícula:** Líneas tenues de guía en gris claro para mantener la rigurosidad matemática.

### 2. Justificación Técnica

Esta composición matemática es la única forma fiel de representar la "mitigación proactiva de interferencia inter-beam". Al desplazar la curva propuesto (`LAM-DRL`) a la derecha, visualizamos cómo el algoritmo reconfigura los diagramas de radiación de los arrays de 64 elementos para alejar los nulos de interferencia de los co-canales, elevando el percentil más bajo de los usuarios.

### 3. ADVERTENCIAS PARA EL USUARIO (Validación)

> ⚠️ **Puntos de Validación Necesarios:**
> 1. **Estilo de Línea:** Para garantizar accesibilidad monocromática (estándar IEEE), sugiero usar línea sólida para el modelo propuesto, discontinua (`--`) para DRL Estándar, y punteada (`..`) para las heurísticas, en lugar de confiar solo en el color.
> 2. **Rango de Interferencia Extrema:** He fijado el inicio del eje X en -10 dB para capturar los usuarios en *shadowing* severo analizados en la sección 5.3. Por favor, confirma si prefieres iniciar en 0 dB si la simulación no contemplaba ruido extremo por debajo del umbral térmico.
> 
> 

---

## FASE 4: Ejecución Silenciosa

' in dash-dot black, and 'Heuristic (PF)' in dotted black. The Proposed LAM-DRL curve is strictly shifted to the right with a sharp rise, showing lower probability at low SINR values]

---

**Por favor, confirma si estás de acuerdo con los hallazgos de la auditoría y las advertencias de interpretación para proceder con la generación final de la estructura de la imagen.**