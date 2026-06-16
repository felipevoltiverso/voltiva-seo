# seo-guidelines.md — Guía SEO para Voltiva Blog

**Versión**: 1.0  
**Última actualización**: Junio 2026

---

## Principios generales

El SEO de Voltiva tiene un objetivo: traer a la persona correcta (alguien evaluando energía solar en Colombia) en el momento correcto (cuando está investigando) y convertirla en un lead de cotización.

**Primero el humano, luego el algoritmo.** Un post bien escrito para personas rankea mejor que uno escrito para bots.

---

## Estructura on-page obligatoria

### H1
- Debe contener el keyword primario
- Una sola por post
- Máximo 60-70 caracteres
- Formato recomendado: `[Beneficio/pregunta] + [keyword] + [contexto Colombia]`

**Ejemplos buenos**:
- "Cuánto cuesta instalar paneles solares en Colombia (2026)"
- "Energía solar para empresas: guía completa para Colombia"
- "Cómo funciona un sistema solar fotovoltaico paso a paso"

---

### Meta title (50-60 caracteres)
```
[Keyword principal] | [Beneficio] | Voltiva
```
**Ejemplos**:
- "Costo Paneles Solares Colombia 2026 | Ahorra Hasta 100% | Voltiva" → muy largo
- "Paneles Solares Colombia: Costos 2026 | Voltiva" → correcto

---

### Meta description (150-160 caracteres)
- Incluir keyword primario
- Incluir propuesta de valor clara
- Incluir CTA implícito ("descubre", "aprende", "calcula")
- No repetir el title textualmente

**Ejemplo**:
"Descubre cuánto cuesta instalar energía solar en Colombia y en cuánto tiempo se paga. Datos reales, sin letra pequeña. Cotiza gratis con Voltiva."

---

### URL slug
- Siempre en minúsculas
- Palabras separadas por guiones `-`
- Sin tildes ni caracteres especiales
- Máximo 5-7 palabras
- Formato: `/blog/[keyword-principal-slug]`

**Ejemplos**:
- ✅ `/blog/cuanto-cuesta-instalar-paneles-solares-colombia`
- ✅ `/blog/energia-solar-para-empresas-colombia`
- ❌ `/blog/energía-solar-¿cuánto-cuesta-en-colombia-2026?`

---

## Densidad de keywords

| Elemento | Frecuencia recomendada |
|----------|----------------------|
| Keyword primario en H1 | 1 vez (exacto o variación) |
| Keyword primario en intro (primeras 100 palabras) | 1 vez |
| Keyword primario en meta title | 1 vez |
| Keyword primario en URL | 1 vez |
| Keyword primario en el cuerpo | Cada 300-400 palabras (natural) |
| Keywords secundarios | Distribuidos naturalmente en H2s y cuerpo |
| LSI keywords | Integrados naturalmente, sin forzar |

**Regla de oro**: Si suena forzado al leerlo en voz alta, quítalo.

---

## Estructura de encabezados

```
H1: [Keyword primario + promesa]
  H2: [Subtema 1 — suele ser la pregunta más básica: ¿qué es?]
    H3: [Detalle opcional]
  H2: [Subtema 2 — beneficios / cómo funciona]
    H3: [Detalle opcional]
  H2: [Subtema 3 — contexto Colombia / costos / regulación]
  H2: [Subtema 4 — proceso con Voltiva / siguiente paso]
  H2: Preguntas frecuentes sobre [keyword]
  H2: Conclusión
```

---

## Longitud de contenido

| Tipo de contenido | Longitud recomendada |
|------------------|---------------------|
| Post informacional (qué es, cómo funciona) | 1,500 - 2,500 palabras |
| Post de pillar / guía completa | 2,500 - 4,000 palabras |
| Post de comparativa o listicle | 1,200 - 2,000 palabras |
| Post de FAQ / respuesta directa | 800 - 1,500 palabras |

Siempre apuntar ~20% más que el promedio de los competidores en el SERP.

---

## Imágenes y alt text

- Toda imagen debe tener alt text descriptivo con keyword cuando sea natural
- Formato recomendado: `[descripción de la imagen] [keyword relacionado] [contexto]`
- **Ejemplos**:
  - ✅ `"Paneles solares instalados en techo residencial en Colombia"`
  - ✅ `"Sistema solar fotovoltaico comercial de 50 kWp en Medellín"`
  - ❌ `"imagen1"` o `"foto paneles"`
- Usar siempre imágenes de proyectos reales de Voltiva (ver image-guidelines.md)
- Comprimir imágenes (WebP preferido, max 200KB)
- Dimensiones hero post: 1200 x 630px

---

## Schema markup recomendado

Para posts de blog: `Article` schema  
Para posts de FAQ: `FAQPage` schema  
Para posts de how-to: `HowTo` schema  

---

## Linking interno

### Mínimo 3 links internos por post
Prioridad de destinos:
1. `/cotiza` — siempre incluir al menos 1 link hacia la cotización
2. Posts relacionados del blog (una vez publicados)
3. Páginas de soluciones (`/soluciones/residencial`, `/soluciones/comercial`)

### Links externos
- Máximo 2-3 links externos por post
- Solo fuentes de alta autoridad: UPME, CREG, Ministerio de Minas, IRENA, Banco Mundial
- Abrir en nueva pestaña (`target="_blank"`)
- Verificar que el link existe antes de incluirlo

---

## Featured snippet — cómo apuntar a ellos

Para keywords con formato pregunta ("¿cuánto cuesta...?", "¿cómo funciona...?"):
1. Incluir la pregunta exacta como H2
2. Responder directamente en el primer párrafo después del H2 (40-60 palabras)
3. Luego expandir con más detalle

**Ejemplo**:
```markdown
## ¿Cuánto cuesta instalar paneles solares en Colombia?

El costo de un sistema solar en Colombia oscila entre $12 millones y $80 millones de pesos, 
dependiendo del tamaño del sistema y el consumo del hogar o empresa. Un sistema residencial 
básico de 3-5 kWp cuesta entre $18 y $35 millones instalado.

[Aquí viene la explicación detallada con tabla de rangos, factores que afectan el precio, etc.]
```

---

## SEO local (Colombia)

- Mencionar ciudades colombianas cuando sea relevante (Medellín, Bogotá, Cali, Barranquilla)
- Incluir contexto de irradiación solar por región cuando aplique
- Mencionar el marco regulatorio colombiano (Ley 1715, CREG)
- Usar COP (pesos colombianos) para cifras económicas, con equivalente en USD si es relevante

---

## Cannibalization check

Antes de crear cualquier brief, verificar:
```bash
# 1. Verificar sitemap live
curl -s "https://voltiva.com.co/sitemap.xml" | grep -o '<loc>[^<]*</loc>' | grep '/blog/'

# 2. Buscar en Google
# Ejecutar búsqueda: site:voltiva.com.co/blog [keyword]

# 3. Revisar registro interno
# Ver: /content-generation/blog/pipeline/content-registry.md
```

---

## Checklist SEO pre-publicación

- [ ] H1 contiene keyword primario
- [ ] Keyword en primeras 100 palabras
- [ ] Meta title 50-60 caracteres
- [ ] Meta description 150-160 caracteres
- [ ] URL slug limpio, sin tildes
- [ ] Mínimo 3 H2s con keywords secundarios/LSI
- [ ] Mínimo 3 links internos (al menos 1 a `/cotiza`)
- [ ] 2-3 links externos a fuentes verificadas
- [ ] Todas las imágenes con alt text
- [ ] Sección FAQ con mínimo 5 preguntas
- [ ] CTA fuerte al final
- [ ] Revisión de cannibalization completada
- [ ] Compliance check completado
