# 🚗 Simulador de Navegación Algorítmica Adaptativa

Este proyecto es un sistema de simulación de navegación urbana autónoma enfocado en resolver problemáticas de distribución logística de última milla y optimización de flujos de transporte. El entorno de pruebas se basa en una red geográfica real modelada en la ciudad de Tijuana, Baja California.

## 📌 Características Principales

* **Topología de Red Real:** Modelado computacional mediante teoría de grafos con **259 nodos** y **413 aristas** que representan intersecciones y calles reales.
* **Inteligencia Adaptativa:** El agente de navegación recalcula trayectorias en milisegundos utilizando algoritmos de ruta más corta, esquivando incidentes viales.
* **Entorno Estocástico:** Simulación de caos urbano mediante la inyección dinámica de 15 obstáculos por turno (Cierres totales en rojo y congestión severa en amarillo).
* **Editor Maestro Integrado:** Incluye una herramienta interactiva construida en HTML/JS con Leaflet/Folium para crear, eliminar y gestionar coordenadas o rutas visualmente, blindada contra la corrupción de índices de red.

## 🧠 Lógica Algorítmica

El núcleo de la IA toma decisiones en tiempo real bajo tres reglas operacionales estrictas:

1. **Optimización Dinámica:** Evaluación constante de la matriz de adyacencia para encontrar la ruta de menor costo euclidiano.
2. **Regla de No Retorno ("Quemar las naves"):** El algoritmo elimina temporalmente del mapa las calles ya visitadas para evitar bucles infinitos y forzar el avance.
3. **Protocolo de Supervivencia (Fallback):** Capacidad de romper reglas restrictivas al detectar un "callejón sin salida", permitiendo desvíos de emergencia o rutas de reversa para garantizar la continuidad del flujo logístico.

## 🛠️ Tecnologías Utilizadas

* **Python:** Lenguaje principal de la lógica de simulación.
* **NetworkX:** Construcción y análisis de la topología de grafos.
* **Matplotlib & Contextily:** Renderizado gráfico de la simulación sobre mapas base reales (OpenStreetMap).
* **Folium & JavaScript:** Motor para el Centro de Control Maestro (creador/editor de topología).

## 🚀 Cómo ejecutar la simulación

1. Clona este repositorio.
2. Instala las dependencias necesarias:
   `pip install networkx matplotlib contextily folium`
3. Ejecuta el script principal de la simulación:
   `python simulador.py`

## 👨‍💻 Autor
* **Nombre:** Ramirez Cardenas Luis Armando
* **Materia:** Patrones de Comportamiento de Datos
* **Profesor:** Adrian Rodriguez Aguiñaga

