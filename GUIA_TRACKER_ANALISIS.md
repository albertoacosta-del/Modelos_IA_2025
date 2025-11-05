# GUÍA PRÁCTICA: ANÁLISIS DE CAÍDA CON TRACKER

## 1. INSTALACIÓN DE TRACKER

### Descargar e Instalar
1. Visita: https://physlets.org/tracker/
2. Descarga la versión para tu sistema operativo (Windows, Mac, Linux)
3. Instala siguiendo las instrucciones (requiere Java)
4. Abre Tracker para verificar la instalación

---

## 2. PREPARACIÓN DEL VIDEO

### Requisitos del Video
- **Formato**: MP4, AVI, MOV (formatos comunes)
- **FPS**: Mínimo 60 fps (ideal 120-240 fps)
- **Resolución**: HD o superior (1080p recomendado)
- **Duración**: Solo la caída (recortar si es necesario)
- **Iluminación**: Uniforme, sin sombras fuertes
- **Fondo**: Contrastante con el objeto

### Elementos Necesarios en el Video
✓ Objeto cayendo completamente visible
✓ Referencia métrica (regla, cinta métrica) en el mismo plano
✓ Cámara fija (sin movimiento)
✓ Encuadre que capture toda la trayectoria

---

## 3. IMPORTAR VIDEO EN TRACKER

### Paso a Paso
1. Abre Tracker
2. **Video → Import Video** (o arrastra el archivo)
3. Selecciona tu archivo de video
4. El video aparecerá en la ventana principal

### Ajustar Clip (Opcional)
- **Clip Settings** (ícono de tijera)
- Selecciona cuadro inicial y final
- Esto reduce el tiempo de análisis

---

## 4. CALIBRACIÓN

### 4.1 Establecer Escala

**Opción A: Calibration Stick**
1. Click en el botón **Calibration** (ícono de regla)
2. Selecciona **New → Calibration Stick**
3. Arrastra los extremos del stick sobre la referencia métrica en el video
4. Ingresa la distancia real (ej: 1.00 m)
5. Click **OK**

**Opción B: Calibration Points**
1. **Calibration → New → Calibration Points**
2. Marca dos puntos de distancia conocida
3. Ingresa la distancia

### 4.2 Establecer Sistema de Coordenadas

1. Click en **Axes** (ícono de ejes coordenados)
2. Arrastra el origen al punto de lanzamiento
3. Ajusta la orientación:
   - Eje Y vertical (positivo hacia arriba)
   - Eje X horizontal
4. Verifica que la escala sea correcta

---

## 5. SEGUIMIENTO DEL OBJETO (TRACKING)

### 5.1 Crear Masa Puntual

1. Click en **Create → Point Mass**
2. Aparecerá un nuevo track llamado "mass A"
3. Renombra (ej: "Pelota_Tenis")

### 5.2 Marcar Posiciones

**Método Manual:**
1. Avanza cuadro por cuadro (teclas **<** y **>**)
2. **Shift + Click** en el centro del objeto en cada cuadro
3. Aparecerá una marca y una línea de trayectoria
4. Continúa hasta el último cuadro

**Método Automático (Autotracker):**
1. **Tracks → Autotracker**
2. Dibuja un rectángulo alrededor del objeto
3. Click **Search**
4. Tracker intentará seguir automáticamente
5. Revisa y corrige manualmente si es necesario

### 5.3 Consejos para Tracking Preciso
- Marca siempre el **mismo punto** del objeto (centro de masa)
- Usa **zoom** para mayor precisión
- Si el objeto rota, marca el centro geométrico
- Verifica que no haya saltos en la trayectoria

---

## 6. VISUALIZACIÓN DE DATOS

### 6.1 Gráficas Automáticas

Tracker genera automáticamente:
- **Posición**: x(t), y(t)
- **Velocidad**: vx(t), vy(t)
- **Aceleración**: ax(t), ay(t)

### 6.2 Personalizar Gráficas

**Cambiar Variables:**
1. Click derecho en el eje de la gráfica
2. Selecciona la variable deseada

**Gráficas Útiles para el Proyecto:**
- **y vs t**: Posición vertical vs tiempo
- **vy vs t**: Velocidad vertical vs tiempo
- **ay vs t**: Aceleración vertical vs tiempo

### 6.3 Ajuste de Curvas (Curve Fitting)

1. Click derecho en la gráfica
2. **Analyze → Curve Fits**
3. Selecciona el modelo:
   - **Parabola** para y(t) en caída libre
   - **Line** para v(t) en caída libre
4. Tracker mostrará la ecuación y R²

---

## 7. EXPORTAR DATOS

### 7.1 Copiar a Hoja de Cálculo

1. Click derecho en la tabla de datos
2. **Copy Data**
3. Pega en Excel/Google Sheets

### 7.2 Exportar como CSV

1. **File → Export → Data File**
2. Selecciona formato CSV
3. Guarda el archivo

### 7.3 Datos Exportados

Columnas típicas:
- `t` (tiempo en segundos)
- `x` (posición horizontal en metros)
- `y` (posición vertical en metros)
- `vx` (velocidad horizontal en m/s)
- `vy` (velocidad vertical en m/s)
- `ax` (aceleración horizontal en m/s²)
- `ay` (aceleración vertical en m/s²)

---

## 8. ANÁLISIS DE ENERGÍA (EN HOJA DE CÁLCULO)

### 8.1 Datos Necesarios
- Masa del objeto: `m` (kg)
- Gravedad: `g = 9.8` m/s²
- Altura inicial: `h₀` (m)
- Datos de Tracker: `t`, `y`, `vy`

### 8.2 Fórmulas en Excel/Sheets

**Velocidad total:**
```
v = SQRT(vx^2 + vy^2)
```

**Altura respecto al suelo:**
```
h = h₀ - y
```
(Nota: Depende de dónde colocaste el origen)

**Energía Potencial:**
```
Ep = m * g * h
```

**Energía Cinética:**
```
Ec = 0.5 * m * v^2
```

**Energía Mecánica:**
```
Em = Ep + Ec
```

**Energía Disipada:**
```
Edis = Em_inicial - Em
```

**Porcentaje de Energía Disipada:**
```
%Edis = (Edis / Em_inicial) * 100
```

### 8.3 Ejemplo de Tabla en Excel

| t (s) | y (m) | vy (m/s) | v (m/s) | h (m) | Ep (J) | Ec (J) | Em (J) | Edis (J) | %Edis |
|-------|-------|----------|---------|-------|--------|--------|--------|----------|-------|
| 0.00  | 0.00  | 0.00     | 0.00    | 2.00  | 1.96   | 0.00   | 1.96   | 0.00     | 0.0%  |
| 0.05  | -0.12 | -0.98    | 0.98    | 2.12  | 2.08   | 0.05   | 2.13   | -0.17    | -8.7% |
| ...   | ...   | ...      | ...     | ...   | ...    | ...    | ...    | ...      | ...   |

---

## 9. GRÁFICAS RECOMENDADAS

### 9.1 En Tracker
1. **y vs t**: Muestra la trayectoria (parábola en caída libre)
2. **vy vs t**: Muestra la aceleración (pendiente = a)
3. **ay vs t**: Muestra si la aceleración es constante

### 9.2 En Hoja de Cálculo
1. **Em vs t**: Muestra pérdida de energía
2. **Ep, Ec vs t**: Muestra transformación de energía
3. **%Edis vs t**: Muestra porcentaje de energía perdida
4. **Comparación entre objetos**: Superponer gráficas de diferentes masas

---

## 10. ANÁLISIS COMPARATIVO (MÚLTIPLES OBJETOS)

### 10.1 Mismo Video, Múltiples Tracks
Si grabaste varios objetos cayendo simultáneamente:
1. **Create → Point Mass** para cada objeto
2. Renombra cada track (ej: "Ping_Pong", "Tenis", "Golf")
3. Marca cada objeto independientemente
4. Tracker generará datos para cada uno

### 10.2 Videos Separados
Si grabaste videos separados:
1. Analiza cada video individualmente
2. Exporta datos de cada uno
3. Combina en una sola hoja de cálculo
4. Asegúrate de que la calibración sea consistente

---

## 11. CÁLCULO DE COEFICIENTE DE ARRASTRE

### 11.1 Identificar Velocidad Terminal (si aplica)

En la gráfica **vy vs t**:
- Si la velocidad se estabiliza (pendiente ≈ 0), se alcanzó velocidad terminal
- Anota el valor de `vt`

### 11.2 Calcular Cd

**Fórmula:**
```
Cd = (2 * m * g) / (ρ * A * vt²)
```

**Donde:**
- `m` = masa del objeto (kg)
- `g` = 9.8 m/s²
- `ρ` = densidad del aire ≈ 1.225 kg/m³
- `A` = área transversal del objeto (m²)
  - Para esfera: `A = π * r²`
- `vt` = velocidad terminal (m/s)

### 11.3 Valores de Referencia de Cd
- Esfera lisa: 0.47
- Pelota de golf: 0.25 (por hoyuelos)
- Disco plano: 1.17
- Forma aerodinámica: 0.04-0.10

---

## 12. TIPS Y SOLUCIÓN DE PROBLEMAS

### Problema: Tracker no detecta el objeto automáticamente
**Solución**: Usa tracking manual (Shift + Click)

### Problema: La escala no es correcta
**Solución**: Verifica que la referencia métrica esté en el mismo plano que el movimiento

### Problema: Datos ruidosos (mucha variación)
**Solución**: 
- Usa **Filters** en Tracker para suavizar datos
- Aumenta fps del video en futuras grabaciones

### Problema: El objeto sale del encuadre
**Solución**: Reduce la altura de caída o aleja la cámara

### Problema: No se alcanza velocidad terminal
**Solución**: Normal para objetos pesados en distancias cortas. Menciona esto en el análisis.

---

## 13. CHECKLIST ANTES DE FINALIZAR

- [ ] Video calibrado correctamente
- [ ] Objeto marcado en todos los cuadros relevantes
- [ ] Datos exportados a hoja de cálculo
- [ ] Energías calculadas (Ep, Ec, Em)
- [ ] Gráficas generadas (mínimo 5)
- [ ] Comparación entre objetos realizada
- [ ] Coeficiente de arrastre calculado (si aplica)
- [ ] Capturas de pantalla de Tracker guardadas
- [ ] Análisis de incertidumbre considerado

---

## 14. RECURSOS ADICIONALES

### Tutoriales en Video
- Canal oficial de Tracker: https://www.youtube.com/user/physlets
- Buscar: "Tracker video analysis tutorial"

### Documentación
- Manual de Tracker: https://physlets.org/tracker/help/frameset.html

### Foros y Comunidad
- Foro de Tracker: https://www.compadre.org/osp/forum/

---

## 15. EJEMPLO DE REPORTE DE RESULTADOS

### Tabla Resumen

| Objeto | Masa (g) | Diámetro (cm) | a_exp (m/s²) | vt (m/s) | Cd | %Edis |
|--------|----------|---------------|--------------|----------|-----|-------|
| Ping-pong | 2.7 | 4.0 | 7.2 | 8.5 | 0.52 | 18.3% |
| Tenis | 58 | 6.7 | 9.1 | - | - | 6.7% |
| Golf | 45 | 4.3 | 9.5 | - | - | 3.2% |

### Interpretación
- La pelota de ping-pong experimenta mayor resistencia del aire (menor aceleración, mayor pérdida de energía)
- La pelota de golf se aproxima más a caída libre ideal
- Solo la pelota de ping-pong alcanzó velocidad terminal en la distancia de caída

---

**¡Éxito con tu proyecto!** 🚀

Esta guía te acompañará paso a paso en el análisis. Recuerda que la precisión en el tracking y la calibración son fundamentales para obtener resultados confiables.
