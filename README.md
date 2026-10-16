<!-- STREAMING_CHUNK:Escribiendo cabecera, insignias y descripción general... -->
# 🧪 Disolucions LAB — Entrenador Interactivo de Disoluciones y Factores de Conversión

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Deploy-success?style=flat&logo=github)](https://pages.github.com/)
[![Materia](https://img.shields.io/badge/Física%20i%20Química-1r%20Batxillerat%20(BAT__FQ%202.1)-indigo)](#)
[![Metodología](https://img.shields.io/badge/Aprendizaje-Factores%20de%20Conversión-blue)](#)
[![Simulador](https://img.shields.io/badge/Laboratorio-Matraz%20Aforado%20SVG-teal)](#)
[![Idiomas](https://img.shields.io/badge/Idiomas-Català%20%7C%20Castellano-orange)](#)
[![Licencia](https://img.shields.io/badge/Licencia-CC%20BY--NC--SA%204.0-lightgrey)](#)

**Disolucions LAB** (o *Dissoldre*) es una aplicación web interactiva de código abierto (*Single-File*). Su objetivo didáctico es que el alumnado de 1.º de Bachillerato domine el cálculo de concentraciones y la preparación de disoluciones mediante el **método de los factores de conversión**, superando la memorización de fórmulas mecánicas o reglas de tres.

---

<!-- STREAMING_CHUNK:Detallando las modalidades de aprendizaje y módulos... -->
## 🎯 Módulos y Arquitectura Pedagógica

La herramienta se organiza en tres áreas de trabajo complementarias accesibles desde la barra superior:

```
┌────────────────────────────────────────────────────────────────────────┐
│                        DISOLUCIONS LAB (IEDIB)                         │
├──────────────────────┬─────────────────────────┬───────────────────────┤
│  🧮 Entrenador de    │  🧪 Simulador de Matraz │  📖 Apuntes y Guía    │
│     Problemas (x2)   │     Aforado Realista    │     Metodológica      │
└──────────────────────┴─────────────────────────┴───────────────────────┘
```

### 1. 🧮 Entrenador de Problemas con Doble Modalidad

El generador algorítmico crea problemas numéricos contextualizados a partir de una base de **17 solutos químicos reales** ($\text{HCl}$, $\text{H}_2\text{SO}_4$, $\text{HNO}_3$, $\text{NaOH}$, $\text{KOH}$, $\text{NaCl}$, $\text{CuSO}_4$, $\text{CaCl}_2$, $\text{KMnO}_4$, $\text{CH}_3\text{COOH}$, glucosa, sacarosa, $\text{NaHCO}_3$, $\text{Na}_2\text{CO}_3$, $\text{KNO}_3$, $\text{NH}_4\text{Cl}$, $\text{MgCl}_2$), ofreciendo dos modalidades de resolución:

* **⚡ Modalidad Directa (Ejercicio Completo):**
  * El estudiante resuelve el problema en su libreta de trabajo.
  * Dispone de un botón opcional de **Pista** para orientar el planteamiento.
  * Introduce directamente el valor numérico en el casillero con validación decimal y tolerancia automática de redondeo ($\pm 3{,}5\%$).
  * Al comprobar, se despliega la **resolución oficial paso a paso en factores de conversión** formateada con KaTeX.

* **🧩 Modalidad Guiada (Constructor de Factores paso a paso):**
  * **Paso 1 (Decisión Estratégica):** Pregunta diagnóstica inicial de opción múltiple para decidir por qué magnitud comenzar y cómo plantear la cadena.
  * **Paso 2 (Constructor Interactivo de Factores):** Pizarra de encadenado donde el alumno selecciona las tarjetas adecuadas de un banco que incluye **distractores realistas** (factores invertidos, magnitudes erróneas). Al encajar cada factor, las unidades del numerador y denominador se **tachan visualmente en rojo** en tiempo real.
  * **Paso 3 (Cálculo Numérico):** Una vez canceladas todas las unidades intermedias y aislada la unidad buscada, se introduce el resultado numérico.

<!-- STREAMING_CHUNK:Explicando el catálogo de problemas y el simulador... -->
### 2. 📚 Tipologías de Problemas Cubiertas (BAT_FQ 2.1)

1. **Concentración Molar ($M$):**
   * Cálculo de molaridad a partir de masa en gramos y volumen en mililitros.
   * Cálculo de masa de soluto puro a pesar en balanza para preparar un matraz determinado.
2. **Porcentaje en Masa (% en masa) y Concentración en masa ($\text{g/L}$):**
   * Relación entre masa de soluto y masa total de disolución ($m_d = m_s + m_{\text{agua}}$).
   * Conversión entre molaridad ($\text{mol/L}$) y concentración en $\text{g/L}$ con la masa molar.
3. **Fracción Molar ($\chi_s$):**
   * Determinación de moles de soluto y disolvente ($M_m(\text{H}_2\text{O}) = 18{,}0\text{ g/mol}$) y cálculo de la proporción adimensional.
4. **Reactivos Comerciales Concentrados (% riqueza y densidad $\rho$):**
   * Cálculo de molaridad a partir de la etiqueta comercial de ácidos y bases concentrados.
   * Cálculo del volumen en $\text{mL}$ a pipetear de un reactivo comercial para preparar una disolución diluida.
5. **Dilución de Disoluciones ($V_1 \cdot M_1 = V_2 \cdot M_2$ mediante factores):**
   * Alícuotas a extraer de disoluciones madre razonadas mediante conservación de moles.

---

### 3. 🧪 Simulador Realista de Matraz Aforado (SVG Interactivo)

Simula el comportamiento físico y óptico en el laboratorio químico:

* **Enrase riguroso:** El menisco del líquido se representa siempre tangente a la **línea de aforo roja grabada en el cuello**.
* **Escala dinámica del recipiente:** Al conmutar la capacidad del matraz ($100\text{ mL}$, $250\text{ mL}$, $500\text{ mL}$, $1000\text{ mL}$), el tamaño físico del matraz en pantalla se escala proporcionalmente.
* **Intensidad óptica (Ley de Beer-Lambert):** Al modificar la masa de soluto o el volumen, el color del líquido se vuelve progresivamente **más oscuro e intenso** cuanto mayor es la molaridad.
* **Cálculo en vivo:** Muestra los moles ($n_s$), la molaridad ($M$) y los $\text{g/L}$ en tiempo real con la cadena de factores asociada.

---

### 4. 📖 Apuntes y Formulario Metodológico

Diseñado para evitar la memorización mecánica de fórmulas cerradas:
* Definiciones formales de concentración (% masa, $C_m$, $M$, $\chi$).
* **Instrucciones Generales en 4 Pasos** para construir factores de conversión razonados, cancelando unidades y distinguiendo con rigor entre $\text{g de soluto puro}$, $\text{g de disolución}$ y $\text{mL de disolución}$.

---

<!-- STREAMING_CHUNK:Documentando herramientas de evaluación y despliegue... -->
## 📊 Herramientas de Evaluación y Gamificación

* **Cronómetro de sesión:** Control de tiempo transcurrido con funciones de pausa/reanudación y reinicio.
* **Marcadores en tiempo real:** Contador de aciertos, récord histórico y racha consecutiva activa (🔥).
* **Desglose de aciertos por categorías:** Seguimiento en vivo de Molaridad, %/$\text{g/L}$, Fracción Molar, Riqueza/$\rho$ y Diluciones.
* **Informe Oficial de Auditoría en PDF:** Al hacer clic en **"Generar PDF de Sesión"**, se abre una ventana de impresión limpia con el nombre del alumno, fecha, tiempo invertido, desglose estadístico y tabla completa con cada intento y su estado de corrección, lista para imprimir o adjuntar como evidencia en Moodle.
* **Conmutador Bilingüe:** Interfaz y enunciados alternables instantáneamente entre **Català** y **Castellano**.


---

## 🛠️ Tecnologías Empleadas

* **HTML5 semántico** y diseño totalmente responsive adaptado a pantallas táctiles, ordenadores y proyectores de aula.
* **JavaScript estándar (Vanilla ES6+):** Motor paramétrico aleatorio, control de estado reactivo y manipulación del DOM nativa.
* **Tailwind CSS (vía CDN):** Estilizado visual modular de alto contraste y aspecto limpio.
* **KaTeX (vía CDN):** Renderizado ultrarrápido y tipográficamente exacto de expresiones químicas y factores fraccionarios sin mostrar sintaxis LaTeX cruda.
* **SVG interactivo nativo:** Generación vectorial del matraz aforado con control de escalado y gradientes de color dinámicos.
* **CSS Print Media Queries:** Generación de informes PDF formateados para entrega escolar sin librerías externas pesadas.

---

## 📄 Autoría y Licencia

* **Autora:** Elena Ruiz Alfaro
* **Materia:** Física i Química 
* **Curso académico:** 2026-2027
* **Licencia:** [Creative Commons Reconeixement-NoComercial-CompartirIgual 4.0 Internacional (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
