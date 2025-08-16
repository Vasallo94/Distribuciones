# Visualizador Interactivo de Distribuciones de Probabilidad

Un pequeño visualizador web para explorar distribuciones estadísticas comunes (Normal, Binomial, Poisson, Exponencial, Uniforme, Gamma, Beta y Geométrica). Permite ajustar parámetros con controles, ver la forma de la densidad/probabilidad en un gráfico interactivo y consultar una ayuda matemática con fórmulas renderizadas.

Este proyecto es una aplicación estática (HTML + CSS + JS) pensada para uso educativo y como herramienta rápida para entender cómo cambian las distribuciones al modificar parámetros.

## Estructura del repositorio

- `index.html` — Aplicación principal: UI, lógica de controles y renderizado de gráficos.
- `README.md` — Este archivo.



## Tecnologías

- HTML5, CSS3
- JavaScript (vanilla)
- Chart.js (CDN)
- MathJax v3 (CDN) — para renderizado LaTeX en la ayuda matemática

## Cómo usar (modo local rápido)

1. Abre `index.html` en tu navegador (doble clic) o sirve la carpeta con un servidor estático local si prefieres (recomendado para evitar restricciones de algunos navegadores):

```bash
# Desde la raíz del proyecto (macOS/Linux)
python3 -m http.server 8000
# luego abre http://localhost:8000
```

2. Interactúa con los selectores de distribución y los sliders de parámetros.
3. Haz clic en "📚 Conceptos Matemáticos" para ver la ayuda con fórmulas matemáticas.
4. Cambia a modo oscuro con el botón "🌙 Modo Oscuro".

## Notas sobre MathJax y fórmulas

- El proyecto usa MathJax v3 (CDN) y carga paquetes útiles (`physics`, `mhchem`, `mathtools`) para ampliar la compatibilidad con macros y notación técnica.
- En etiquetas de UI (labels, sliders) se usan símbolos Unicode (μ, σ, λ, α, β) en lugar de notación LaTeX, porque MathJax no procesa automáticamente contenido insertado por innerHTML en todos los contextos. Las fórmulas largas y bloques matemáticos sí usan delimitadores LaTeX (`$...$`, `$$...$$`) y se procesan con `MathJax.typesetPromise()`.
- Para añadir nuevas macros o paquetes: edita la configuración `window.MathJax` al inicio de `index.html`.

## Contribuir

Si quieres que cambie el diseño, añada nuevas distribuciones o mejore la accesibilidad, abre un issue aquí (o pásame los cambios que quieras) y los aplicaré.

## Página publicada

La versión pública del proyecto está desplegada en GitHub Pages:

https://Vasallo94.github.io/Distribuciones/

Visita esa URL para ver la aplicación en producción. Si no ves cambios recientes, fuerza la recarga en tu navegador (Cmd+Shift+R en macOS) o limpia la caché.

Si prefieres, también puedes acceder directamente al archivo `index.html` en el repositorio y abrirlo localmente.

