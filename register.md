```markdown
**Title**: Optimización de Enlaces NTN mediante Inteligencia Artificial: Automatización de Gestión de Recursos para Incremento de Throughput y Reducción de Interferencias

**Description**: Las Redes No Terrestres (NTN) constituyen un pilar esencial para la cobertura global en 6G, pero enfrentan importantes desafíos en la gestión dinámica de recursos debido a la alta movilidad, variabilidad de canales y interferencias. Este trabajo propone un framework basado en Aprendizaje por Refuerzo Profundo (DRL) guiado por Large Artificial Intelligence Models (LAM) para la optimización autónoma en tiempo real de potencia, ancho de banda y beamforming en enlaces NTN. Formulado como un Proceso de Decisión de Markov multi-agente, el sistema maximiza el throughput sum-rate y fairness mientras minimiza interferencias y probabilidad de outage. Los resultados de simulación en escenarios LEO realistas demuestran mejoras de 42-64% en throughput y reducción significativa de interferencias respecto a baselines heurísticos y DRL estándar.

**General Objective**: Desarrollar e implementar un framework de inteligencia artificial para la optimización autónoma de la gestión de recursos en enlaces de Redes No Terrestres (NTN), incrementando el throughput y reduciendo interferencias.

**Specific Objectives**: 
- Modelar la arquitectura NTN, el canal de propagación y el problema de optimización como un MDP multi-agente.
- Diseñar e integrar un esquema DRL guiado por Large AI Models con predicción de canal mediante LSTM para automatización de potencia, ancho de banda y beamforming.
- Evaluar el rendimiento del framework propuesto en escenarios de simulación realistas con constelaciones LEO frente a baselines heurísticos y DRL estándar.
- Analizar las mejoras en throughput, eficiencia espectral, fairness, reducción de interferencias y complejidad computacional del sistema.

**Justification**: Las NTN son fundamentales para lograr la visión de conectividad ubicua y resiliente de 6G, especialmente en zonas remotas, marítimas y aéreas. La gestión tradicional de recursos resulta ineficiente ante la dinámica orbital y variabilidad de canales. Esta investigación aporta una solución basada en IA avanzada que mejora significativamente el rendimiento del sistema, facilitando la integración TN-NTN y habilitando aplicaciones de misión crítica. Su impacto técnico fortalece la soberanía tecnológica y contribuye al cierre de la brecha digital global.

**Methodology**: Se emplea un enfoque basado en simulación y modelado matemático. El problema se formula como un Proceso de Decisión de Markov (MDP) multi-agente. La solución propuesta integra Deep Reinforcement Learning guiado por Large AI Models (LAM), predicción de canal con LSTM y beamforming adaptativo. La evaluación se realiza en un simulador Python con modelos de propagación ITU-R, mecánica orbital precisa y escenarios heterogéneos de usuarios. Se comparan métricas clave (throughput, SINR, Jain index, interferencia) contra baselines establecidos.

**Scope**: Simulación de constelaciones LEO con hasta 200 usuarios y optimización multi-agente en escenarios nominales y de alta carga (máx. 100 caracteres).

**Activities**: 
1. Revisión del estado del arte y definición del modelo de sistema.
2. Formulación matemática del problema y diseño del framework LAM-DRL.
3. Implementación del simulador y entrenamiento de los agentes.
4. Ejecución de experimentos y análisis comparativo de resultados.
5. Discusión de limitaciones y propuestas de trabajos futuros.

**Resources**: 
- Software: Python, bibliotecas de machine learning (PyTorch/TensorFlow), simuladores de órbita y propagación ITU-R.
- Datos: Modelos de canal satelital, escenarios de tráfico heterogéneo y constelaciones LEO.
- Hardware: Plataforma de cómputo para entrenamiento de modelos DRL (GPU recomendada).

**Limitations**: Los resultados corresponden a entornos de simulación y requieren validación en hardware-in-the-loop o pruebas en órbita. El overhead computacional de LAM-DRL puede limitar su implementación en satélites con restricciones energéticas severas. La escalabilidad a mega-constelaciones y el manejo de estimación de canal imperfecta constituyen riesgos técnicos identificados.
```