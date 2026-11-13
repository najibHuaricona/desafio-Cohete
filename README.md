# Simulador NASA 1962 — Métodos Numéricos

Aplicación educativa para simular el movimiento vertical de un cohete experimental y comparar Euler, Heun y Runge-Kutta de cuarto orden (RK4) con la solución analítica.

## Cómo ejecutar
1. Abre `index.html` con Google Chrome, Edge o Firefox.
2. Modifica los parámetros y pulsa **Ejecutar simulación**.
3. Cambia el tamaño de paso para estudiar cómo varían los errores.
4. Usa **Descargar resultados CSV** para guardar las iteraciones.

No requiere instalar dependencias, servidor, conexión a Internet ni bibliotecas externas.

## Modelo
- `m dv/dt = T - mg - kv`
- `dy/dt = v`

Para `k > 0`:
`v(t) = v_inf + (v0 - v_inf) exp(-(k/m)t)`, donde `v_inf = (T - mg)/k`.

`y(t) = y0 + v_inf t + (v0 - v_inf)(1 - exp(-(k/m)t))/(k/m)`.

Cuando `k = 0`, la aplicación utiliza la solución de aceleración constante.

## Funciones
- Parámetros editables: masa, empuje, gravedad, resistencia, velocidad y altura iniciales, tiempo final y paso.
- Métodos Euler, Heun y RK4.
- Solución analítica de velocidad y altura.
- Tablas de iteraciones y errores absolutos.
- Gráficas comparativas de velocidad y altura.
- Verificación de precisión: error de velocidad menor que 0,5 m/s y error de altura menor que 5 m.
- Exportación CSV y diseño adaptable a móviles y computadoras.

## Publicar en GitHub Pages
1. Crea un repositorio público, por ejemplo `simulador-nasa-1962`.
2. Sube `index.html` y `README.md` a la raíz.
3. Entra en **Settings → Pages**.
4. En **Build and deployment**, selecciona **Deploy from a branch**.
5. Selecciona la rama `main` y la carpeta `/ (root)`, y guarda.
6. Espera a que GitHub Pages publique el sitio. El enlace aparecerá en esa sección.

## Alcance y limitaciones
Modelo académico simplificado: considera masa, empuje, gravedad y resistencia lineal constantes. No modela combustible consumido, masa variable, viento, cambios atmosféricos ni maniobras reales. No debe utilizarse para diseñar ni operar cohetes reales.
