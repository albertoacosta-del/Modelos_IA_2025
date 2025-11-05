# ESTUDIO DEL MOVIMIENTO DE CAÍDA CON RESISTENCIA DEL AIRE Y ANÁLISIS ENERGÉTICO
## (Utilizando herramientas digitales: Tracker Video Analysis)

---

## 1. OBJETIVO GENERAL

Analizar el movimiento de caída de objetos con diferentes masas considerando la resistencia del aire, estudiando la transformación y pérdida de energía mecánica durante el proceso, y comparando los resultados experimentales con el modelo teórico de caída libre ideal.

---

## 2. OBJETIVOS ESPECÍFICOS

1. **Registrar y analizar** el movimiento de caída de al menos 3 objetos con diferentes masas utilizando video de alta velocidad y el software Tracker.

2. **Calcular la energía potencial, cinética y mecánica** en diferentes puntos de la trayectoria para cada objeto.

3. **Cuantificar la pérdida de energía** debido a la fricción del aire y determinar su relación con la masa del objeto.

4. **Comparar la aceleración experimental** de cada objeto con la aceleración gravitacional teórica (g = 9.8 m/s²).

5. **Determinar el coeficiente de arrastre** aproximado para cada objeto mediante el análisis de la velocidad terminal (si se alcanza).

6. **Establecer la relación** entre la masa del objeto y el efecto de la resistencia del aire en su movimiento.

---

## 3. MARCO TEÓRICO

### 3.1 Caída Libre Ideal vs. Caída Real

En condiciones ideales (vacío), un objeto en caída libre experimenta únicamente la fuerza gravitacional, resultando en un movimiento uniformemente acelerado con aceleración constante g ≈ 9.8 m/s².

**Ecuaciones de caída libre ideal:**
- Posición: **h = h₀ - ½gt²**
- Velocidad: **v = gt**
- Energía potencial: **Ep = mgh**
- Energía cinética: **Ec = ½mv²**
- Energía mecánica: **Em = Ep + Ec = constante**

Sin embargo, en condiciones reales, la **resistencia del aire** (fuerza de arrastre) actúa en dirección opuesta al movimiento, causando:
- Reducción de la aceleración efectiva
- Pérdida de energía mecánica (disipación como calor)
- Posible alcance de velocidad terminal

### 3.2 Fuerza de Arrastre

La fuerza de resistencia del aire se puede modelar como:

**Fd = ½ρCdAv²**

Donde:
- ρ = densidad del aire (≈ 1.225 kg/m³)
- Cd = coeficiente de arrastre (depende de la forma del objeto)
- A = área transversal del objeto
- v = velocidad del objeto

### 3.3 Ecuación de Movimiento con Resistencia

La segunda ley de Newton para un objeto en caída con resistencia del aire:

**ma = mg - Fd**

**a = g - (ρCdAv²)/(2m)**

Esta ecuación muestra que:
- La aceleración NO es constante
- Objetos más masivos experimentan menor efecto de la resistencia del aire
- A mayor velocidad, mayor es la fuerza de arrastre

### 3.4 Velocidad Terminal

Cuando Fd = mg, la aceleración se hace cero y el objeto alcanza su velocidad terminal:

**vt = √(2mg/(ρCdA))**

### 3.5 Análisis Energético

Durante la caída con resistencia del aire:
- **Energía potencial inicial**: Ep₀ = mgh₀
- **Energía cinética en cualquier punto**: Ec = ½mv²
- **Energía disipada por fricción**: Edis = Ep₀ - (Ep + Ec)

La energía mecánica NO se conserva:
**Em(t) = Ep(t) + Ec(t) < Em₀**

---

## 4. MATERIALES

### 4.1 Objetos de Prueba
- **Objeto 1**: Pelota de ping-pong (masa ≈ 2.7 g, baja densidad)
- **Objeto 2**: Pelota de tenis (masa ≈ 58 g, densidad media)
- **Objeto 3**: Pelota de golf o bola de acero (masa ≈ 45-100 g, alta densidad)
- **Alternativas**: Esferas de diferentes materiales con tamaños similares

### 4.2 Equipo de Medición
- **Cámara de video**: Smartphone con grabación a 60 fps mínimo (preferible 120-240 fps)
- **Trípode o soporte** para mantener la cámara fija
- **Cinta métrica o regla** de al menos 2-3 metros para calibración
- **Balanza digital** para medir masa de los objetos
- **Calibre o vernier** para medir dimensiones de los objetos

### 4.3 Software
- **Tracker Video Analysis** (gratuito, disponible en https://physlets.org/tracker/)
- **Hoja de cálculo** (Excel, Google Sheets, LibreOffice Calc)
- **Software de edición de video** (opcional, para recortar clips)

### 4.4 Espacio Experimental
- Altura mínima de caída: **2-3 metros** (escalera, balcón, ventana)
- Espacio libre de obstáculos
- Fondo contrastante para facilitar el seguimiento en Tracker
- Buena iluminación natural o artificial

---

## 5. PROCEDIMIENTO EXPERIMENTAL

### 5.1 Preparación

1. **Caracterización de objetos**:
   - Medir y registrar la masa de cada objeto
   - Medir diámetro/dimensiones para calcular área transversal
   - Calcular densidad aproximada

2. **Configuración del espacio**:
   - Seleccionar altura de caída (medir con precisión)
   - Colocar referencia métrica visible en el video (regla o cinta)
   - Posicionar cámara perpendicular al plano de caída
   - Asegurar que toda la trayectoria sea visible en el encuadre

3. **Configuración de cámara**:
   - Usar máxima velocidad de cuadros disponible (fps)
   - Fijar exposición y enfoque
   - Realizar video de prueba

### 5.2 Grabación

1. **Para cada objeto** (repetir 3 veces mínimo):
   - Sostener el objeto a la altura inicial sin velocidad inicial
   - Iniciar grabación
   - Soltar el objeto (no lanzar)
   - Grabar hasta que el objeto llegue al suelo o salga del encuadre
   - Detener grabación

2. **Grabar video de calibración**:
   - Filmar la referencia métrica en el mismo plano de caída
   - Asegurar que sea claramente visible

### 5.3 Análisis en Tracker

1. **Importar video** en Tracker

2. **Calibrar**:
   - Usar herramienta de calibración con la referencia métrica
   - Establecer sistema de coordenadas (origen en punto de lanzamiento)

3. **Seguimiento del objeto**:
   - Marcar posición del centro de masa en cada cuadro
   - Tracker generará automáticamente datos de:
     - Posición (x, y) vs tiempo
     - Velocidad (vx, vy) vs tiempo
     - Aceleración (ax, ay) vs tiempo

4. **Exportar datos** a formato CSV o copiar a hoja de cálculo

### 5.4 Análisis de Datos

Para cada objeto, calcular:

1. **Cinemática**:
   - Gráficas posición vs tiempo (y vs t)
   - Gráficas velocidad vs tiempo (vy vs t)
   - Gráficas aceleración vs tiempo (ay vs t)
   - Aceleración promedio y compararla con g

2. **Energía en cada punto**:
   - Ep(t) = mg(h₀ - y(t))
   - Ec(t) = ½m[v(t)]²
   - Em(t) = Ep(t) + Ec(t)
   - Edis(t) = Em₀ - Em(t)

3. **Porcentaje de energía disipada**:
   - %Edis = [Edis(t)/Em₀] × 100%

4. **Análisis de velocidad terminal** (si aplica):
   - Identificar si se alcanza velocidad constante
   - Calcular Cd usando vt = √(2mg/(ρCdA))

---

## 6. RESULTADOS ESPERADOS

### 6.1 Cinemática

- **Objetos más ligeros** (pelota de ping-pong):
  - Aceleración significativamente menor que g
  - Posible alcance de velocidad terminal
  - Desviación notable del modelo de caída libre

- **Objetos más pesados** (bola de acero):
  - Aceleración más cercana a g
  - Menor probabilidad de alcanzar velocidad terminal en distancias cortas
  - Comportamiento más cercano a caída libre ideal

### 6.2 Energía

- **Pérdida de energía mecánica** en todos los casos, pero:
  - Mayor pérdida porcentual en objetos ligeros
  - Menor pérdida porcentual en objetos pesados

- **Gráfica Em vs t**:
  - Caída libre ideal: línea horizontal (Em constante)
  - Caída real: curva descendente (Em disminuye)
  - Pendiente más pronunciada para objetos ligeros

### 6.3 Relación Masa-Resistencia

- Gráfica de **aceleración promedio vs masa**: tendencia creciente hacia g
- Gráfica de **%Edis vs masa**: tendencia decreciente
- Tabla comparativa de coeficientes de arrastre

---

## 7. ANÁLISIS Y DISCUSIÓN

### 7.1 Preguntas de Investigación

1. ¿Cómo varía la aceleración efectiva con la masa del objeto?
2. ¿Qué porcentaje de energía se pierde por fricción en cada caso?
3. ¿Algún objeto alcanza velocidad terminal? ¿Cuál es su valor?
4. ¿Cómo se comparan los coeficientes de arrastre calculados con valores de referencia?
5. ¿A partir de qué masa el efecto de la resistencia del aire se vuelve despreciable?

### 7.2 Fuentes de Error

- Resolución temporal del video (fps limitados)
- Precisión en el marcado de posiciones en Tracker
- Efectos de rotación del objeto (no considerados en el modelo)
- Variaciones en la densidad del aire
- Incertidumbre en mediciones de masa y dimensiones

---

## 8. CONCLUSIONES ESPERADAS

1. **Validación del modelo**: La resistencia del aire tiene un efecto medible y significativo, especialmente en objetos de baja masa/densidad.

2. **Conservación de energía**: La energía mecánica NO se conserva en caída real; la energía "perdida" se disipa como calor debido a la fricción con el aire.

3. **Dependencia de la masa**: Objetos más masivos se aproximan mejor al modelo de caída libre ideal, confirmando que la resistencia del aire afecta más a objetos ligeros.

4. **Aplicación de Tracker**: El software permite un análisis cuantitativo preciso del movimiento, validando o refutando modelos teóricos.

5. **Importancia del contexto**: El modelo de caída libre es una idealización útil, pero debe aplicarse con precaución según las condiciones reales del experimento.

---

## 9. REFERENCIAS

1. Serway, R. A., & Jewett, J. W. (2018). *Physics for Scientists and Engineers*. Cengage Learning.

2. Halliday, D., Resnick, R., & Walker, J. (2013). *Fundamentals of Physics*. Wiley.

3. Brown, D. (2024). *Tracker Video Analysis and Modeling Tool*. https://physlets.org/tracker/

4. Munson, B. R., et al. (2013). *Fundamentals of Fluid Mechanics*. Wiley.

5. Benson, H. (2012). *University Physics*. Wiley.

---

## 10. CRONOGRAMA SUGERIDO

| Semana | Actividad |
|--------|-----------|
| 1 | Preparación de materiales, caracterización de objetos, pruebas de cámara |
| 2 | Grabación de videos experimentales (múltiples repeticiones) |
| 3 | Análisis de videos en Tracker, exportación de datos |
| 4 | Cálculos de energía, gráficas, análisis estadístico |
| 5 | Redacción de informe, conclusiones, preparación de presentación |

---

## ANEXOS SUGERIDOS

### A. Tabla de Datos Experimentales
- Características de cada objeto (masa, diámetro, área, densidad)
- Altura de caída
- Velocidad de cuadros del video (fps)

### B. Gráficas Principales
- Posición vs tiempo (comparación de los 3 objetos)
- Velocidad vs tiempo (comparación de los 3 objetos)
- Energía mecánica vs tiempo (comparación de los 3 objetos)
- Porcentaje de energía disipada vs masa

### C. Capturas de Tracker
- Pantallazos del proceso de análisis
- Trayectorias marcadas

### D. Cálculos Detallados
- Ejemplo de cálculo de energía para un punto
- Cálculo de coeficiente de arrastre
- Análisis de incertidumbre

---

**Nota Final**: Este proyecto ampliado cumple con los requisitos de un trabajo de investigación experimental riguroso, incorporando análisis energético, consideración de fuerzas reales (fricción), uso de herramientas digitales profesionales (Tracker), y estudio comparativo con variación de parámetros (masa). Va más allá de una práctica simple al requerir análisis cuantitativo profundo y comparación crítica entre modelo teórico y realidad experimental.
