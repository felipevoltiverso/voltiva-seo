# Voltiva SEO Content System — README

**Versión**: 1.0  
**Sitio**: voltiva.com.co  
**Creado**: Junio 2026

---

## ¿Qué es esto?

Sistema completo de generación de contenido SEO para el blog de Voltiva. Diseñado para producir posts que rankeen en Google Colombia y conviertan lectores en leads de cotización.

La arquitectura espeja el sistema de Selia (salud mental) adaptado al sector de energía solar en Colombia.

---

## Estructura de archivos

```
voltiva-seo/
├── README.md                              ← Estás aquí
├── .meta/
│   └── CONTEXT.md                         ← Contexto completo de Voltiva
└── content-generation/
    └── blog/
        ├── brief-generator-agent.md        ← AGENTE 1: Genera briefs de keywords
        ├── post-generator-agent.md         ← AGENTE 2: Genera posts completos
        ├── context/
        │   ├── master-prompt.md            ← Rol, guardrails, tono general
        │   ├── brand-voice.md              ← Voz y tono de Voltiva
        │   ├── seo-guidelines.md           ← Reglas SEO on-page
        │   ├── compliance.md               ← Qué NO decir
        │   ├── source-verification.md      ← Protocolo anti-alucinación
        │   └── image-guidelines.md         ← Estilo fotográfico y visual
        ├── briefs/                         ← Briefs generados (vacío al inicio)
        ├── posts/                          ← Posts generados (vacío al inicio)
        └── pipeline/
            ├── topics-queue.md             ← 20 keywords priorizados listos
            ├── status-tracker.md           ← Estado de cada pieza de contenido
            └── content-registry.md         ← Inventario de contenido publicado
```

---

## Cómo usar el sistema

### Flujo estándar

```
1. Elegir keyword del topics-queue.md
        ↓
2. Invocar Brief Generator Agent
        ↓
3. Revisión humana del brief (equipo Voltiva)
        ↓
4. Invocar Post Generator Agent con brief aprobado
        ↓
5. Revisión editorial final
        ↓
6. Publicar en CMS → Actualizar content-registry.md
```

### Paso 1: Elegir keyword

Abrir `pipeline/topics-queue.md` y elegir un keyword de la sección de Prioridad Alta.

### Paso 2: Generar brief

Invocar el Brief Generator Agent con este input:

```
Keyword: [keyword elegido]
Search Volume: [volumen del topics-queue]
Keyword Difficulty: [dificultad del topics-queue]
Search Intent: [intención del topics-queue]
Target URL: nueva
```

El agente generará el brief completo. Guardarlo en:
`/content-generation/blog/briefs/YYYY-MM-DD-keyword-slug.md`

### Paso 3: Revisión del brief

El equipo de Voltiva revisa:
- ¿El outline tiene sentido para nuestra audiencia?
- ¿Los CTAs están en los lugares correctos?
- ¿El ángulo es diferenciador?
- ¿Hay datos o afirmaciones que cambiar?

Aprobar con status `brief_aprobado` en `status-tracker.md`.

### Paso 4: Generar post

Invocar el Post Generator Agent con el brief aprobado completo.

Guardar en: `/content-generation/blog/posts/YYYY-MM-DD-keyword-slug.md`

### Paso 5: Revisión editorial

Verificar:
- ✅ Tono Voltiva correcto
- ✅ Datos técnicos verificados
- ✅ Compliance checklist completo
- ✅ Links internos funcionando
- ✅ Meta tags correctos

### Paso 6: Publicar

- Publicar en CMS (WordPress / Webflow / el que use Voltiva)
- Actualizar `content-registry.md` con URL publicada
- Actualizar `status-tracker.md` → `publicado`
- Monitorear posición en Google Search Console a las 4 semanas

---

## Primer mes recomendado

Atacar estos 3 posts en orden:

| Semana | Keyword | Razón |
|--------|---------|-------|
| 1-2 | "como funciona la energia solar" | Alto volumen, KD media, awareness |
| 3-4 | "cuanto cuesta instalar paneles solares en colombia" | Alto valor comercial |
| 5-6 | "beneficios energia solar colombia" | Complementa los anteriores |

---

## Fuentes de autoridad para citar

| Institución | URL | Tipo de dato |
|------------|-----|--------------|
| UPME | upme.gov.co | Capacidad instalada, política energética |
| CREG | creg.gov.co | Regulación, net metering |
| IDEAM | ideam.gov.co | Irradiación solar por región |
| Min. Minas | minminas.gov.co | Política energética, Ley 1715 |
| IRENA | irena.org | Datos globales, tendencias |
| Banco Mundial | worldbank.org | Datos de energía renovable |

---

## Proof points de Voltiva (siempre actualizados)

Actualizar cuando cambien los números reales:

- +34 proyectos instalados en Colombia
- +400 kWp instalados en toda Colombia
- Cotización online en minutos
- Monitoreo 24/7 post-instalación
- Financiación sin cuota inicial
- Sistema diseñado a la medida

---

## Contacto del equipo

Para preguntas sobre el sistema, actualizar context files o aprobar contenido:
- Felipe (Growth & Marketing) — responsable del sistema SEO
