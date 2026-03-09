# 🚀 Dashboard de Sprints - Aceleración Digital TVN

## ✅ Lo que se creó

### 1. Dashboard HTML Moderno
📄 `dashboard_sprints_tvn.html`

**Características:**
- ✨ Diseño moderno con glassmorphism y gradientes
- 📊 Hero KPIs (total sprints, en curso, avance promedio, prioridad alta)
- 🎯 Cards de sprints con estado visual, progreso y riesgos
- 🔍 Filtros: Todos, En Curso, Pendientes, Prioridad Alta
- ⚠️ Sección destacada de riesgos/bloqueadores por sprint
- 📱 100% responsive
- 🎨 Colores corporativos TVN

### 2. Datos JSON Estructurados
📊 `sprints_data.json`

Generado automáticamente desde tu Excel con:
- 8 sprints del proyecto de Migración de Plataformas Web
- Estadísticas agregadas
- Fechas, responsables, dependencias, métricas

---

## 🎯 Cómo usar

### Para presentar en comités

1. **Abrir el dashboard:**
   ```bash
   open ~/. openclaw/workspace/dashboard_sprints_tvn.html
   ```

2. **Presentación:**
   - KPIs arriba dan contexto general
   - Scroll para ver cada sprint en detalle
   - Usa filtros para enfocarte (ej: solo "En Curso" o "Prioridad Alta")
   - Riesgos destacados en rojo para visibilidad inmediata

### Para actualizar datos

**Opción A - Desde Excel (recomendado):**
1. Editar tu Excel original
2. Enviarme el Excel actualizado
3. Yo regenero el JSON y refrescás el dashboard

**Opción B - Editar JSON directo:**
1. Abrir `sprints_data.json`
2. Modificar fechas, avances, estados, etc.
3. Refrescar navegador

---

## 📊 Estructura de datos

Cada sprint tiene:
```json
{
  "id": "P1-S1",
  "sprint": "Nombre del sprint",
  "objetivo": "Descripción del objetivo",
  "responsables": "Equipo responsable",
  "fecha_inicio": "2025-03-10",
  "fecha_termino": "2025-04-11",
  "estado": "En curso | Pendiente | Completado | Bloqueado",
  "prioridad": "Alta | Media | Baja",
  "avance": 0.15,  // 15%
  "dependencias": "P1-S2 · P1-S3",
  "riesgos": "Descripción de riesgos",
  "metricas": "Criterios de éxito",
  "notas": "Observaciones"
}
```

---

## 🎨 Personalización

### Cambiar colores
Editar variables CSS en el `<style>`:
```css
:root {
    --tvn-blue: #0066CC;
    --tvn-red: #E31B23;
    /* etc */
}
```

### Agregar más filtros
En la sección `.filters`, agregar botones:
```html
<button class="filter-btn" onclick="filterSprints('completado')">Completados</button>
```

### Modificar KPIs
Función `renderKPIs()` en el JavaScript.

---

## 🚀 Próximas mejoras (opcionales)

1. **Timeline Gantt visual** - Barras horizontales mostrando duración y overlap
2. **Vista de dependencias** - Diagrama de flujo interactivo
3. **Gráfico de burn-down** - Evolución del avance en el tiempo
4. **Export a PDF** - Para compartir offline
5. **Dashboard de equipo** - Carga de trabajo por responsable
6. **Alertas automáticas** - Destacar sprints próximos a vencer

---

## 📁 Archivos

```
~/.openclaw/workspace/
├── dashboard_sprints_tvn.html       # ← Dashboard (abrir en navegador)
├── sprints_data.json                # ← Datos (auto-generado desde Excel)
└── README_SPRINTS_DASHBOARD.md      # ← Este archivo
```

---

## 💡 Tips para la presentación

1. **Abre en pantalla completa** (F11 en Chrome/Firefox)
2. **Usa los filtros en vivo** durante la presentación para mostrar interactividad
3. **Destaca los riesgos** - están visualmente resaltados en rojo
4. **Menciona el avance promedio** del KPI hero (actualmente 1.9%)
5. **Proyecta confianza** - es un dashboard moderno vs Excel estático

---

¿Necesitás algo más? Mejoras visuales, más funciones, o cambios de diseño.
