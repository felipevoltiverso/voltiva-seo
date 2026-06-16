# CONTEXT.md — Voltiva SEO Content System

**Versión**: 1.0  
**Fecha de creación**: Junio 2026  
**Sitio web**: https://voltiva.com.co  
**Sitemap**: https://voltiva.com.co/sitemap.xml

---

## ¿Quién es Voltiva?

Voltiva es una empresa colombiana de energía solar que diseña independencia energética. No venden paneles: son socios estratégicos de cada proyecto solar en Colombia.

### Misión
Transformar la relación de las personas y empresas con su consumo energético mediante soluciones de energía solar especializada de alto rendimiento. Entregan estabilidad, solidez y certeza técnica a través de un servicio transparente y digital, permitiendo que cada socio estratégico tome el control total de su energía eléctrica, reduzca sus costos y asegure un respaldo de alta confiabilidad.

### Visión
Liderar la transición hacia la energía solar en Colombia, logrando que hogares y empresas dejen de depender de la red eléctrica convencional. Estandarizar la generación propia de energía en el país, asegurando que cada proyecto solar instalado sea sinónimo de libertad financiera, cero apagones y rentabilidad garantizada por décadas.

### Declaración de marca
"En Voltiva, redefinimos las reglas del juego para que la libertad energética sea, finalmente, la norma."

### Números clave (proof points)
- +34 proyectos instalados
- +400 kWp instalados en toda Colombia
- Financiación sin cuota inicial
- Monitoreo 24/7
- Sistema diseñado a la medida
- Equipos de máxima calidad

---

## Audiencia objetivo

### Segmento residencial
- Propietarios de vivienda (estratos 4-6) en Colombia
- Familias con facturas de energía altas (>$200,000 COP/mes)
- Personas interesadas en valorizar su propiedad
- Perfil: 35-60 años, propietario, preocupado por costos de servicios públicos

### Segmento comercial/empresarial
- Gerentes y propietarios de PYMES con alto consumo energético
- Industria, manufactura, retail, hoteles, clínicas
- Empresas con compromisos de sostenibilidad ESG
- Perfil: tomador de decisiones, analiza ROI, busca certeza técnica

### Características psicográficas compartidas
- Cansados de tarifas eléctricas que suben cada año
- Buscan certeza y profesionalismo (no vendedores de paneles baratos)
- Valoran la transparencia en precios y procesos
- Quieren entender el retorno de inversión antes de decidir

---

## Arquitectura del sitio (URLs conocidas)

### Páginas principales
- `/` — Home
- `/cotiza` — Cotización online
- `/proyectos` — Galería de proyectos instalados
- `/nosotros` — Quiénes somos
- `/blog` — Blog de contenidos SEO
- `/contacto` — Contacto

### Servicios / soluciones (inferidos del brandbook)
- `/soluciones/residencial` — Energía solar para hogares
- `/soluciones/comercial` — Energía solar para empresas
- `/soluciones/industrial` — Soluciones industriales
- `/soluciones/fuera-de-red` — Off-grid / rural

### Calculadoras y herramientas (oportunidad)
- `/calculadora-ahorro` — Calculadora de ahorro solar
- `/calculadora-roi` — Retorno de inversión solar

> **Nota**: Verificar URLs reales haciendo fetch del sitemap antes de incluir links internos en cualquier brief o post.

---

## Geografía objetivo

**Principal**: Colombia (todas las ciudades)  
**Prioridad 1**: Medellín, Bogotá, Cali, Barranquilla, Bucaramanga  
**Prioridad 2**: Ciudades intermedias con alta irradiación solar (eje cafetero, costa caribe, llanos)

---

## Competencia directa (Colombia)

- Celsia Solar
- EPM Solar / Enel Green Power
- Solartime Colombia
- Enerlink
- Instaladores locales sin marca fuerte

**Oportunidad de diferenciación**: La mayoría de competidores habla en tecnicismos o es genérica. Voltiva tiene voz y posicionamiento claros: socio estratégico, no proveedor.

---

## Objetivos SEO del blog

1. **Atraer tráfico cualificado** de personas que están evaluando la energía solar
2. **Educar** sobre beneficios, costos, proceso y regulación en Colombia
3. **Generar leads** hacia la cotización online
4. **Posicionar a Voltiva** como autoridad técnica en energía solar en Colombia
5. **Capturar demanda existente** en keywords de alto volumen (qué es, cómo funciona, cuánto cuesta)

### KPIs del blog
- Posición top 10 en keywords objetivo dentro de 8-12 semanas
- CTR desde SERP: 5-10%
- Conversión blog → cotización: 2-5%
- Tráfico orgánico mensual: crecimiento sostenido MoM

---

## Tono de los contenidos del blog

Siguiendo los principios de voz de Voltiva (ver brand-voice.md):
- **Directo y sin rodeos**: vamos al grano, sin jerga corporativa vacía
- **Seguro y confiable**: el lector siente que está en manos de profesionales
- **Aterrizado al beneficio real**: traducir tecnología en impacto en la factura
- **Ágil y tecnológico**: resaltar la facilidad del proceso digital

**Registros permitidos en el blog**: explicativo, educativo, consultivo  
**Nunca**: corporativo-abstracto, informal/básico, prometedor de cosas sin respaldo

---

## Sistema de archivos del proyecto

```
voltiva-seo/
├── .meta/
│   └── CONTEXT.md                    ← Este archivo
├── content-generation/
│   └── blog/
│       ├── context/
│       │   ├── master-prompt.md      ← Rol, guardrails, tono general
│       │   ├── brand-voice.md        ← Voz y tono de Voltiva
│       │   ├── seo-guidelines.md     ← Reglas SEO on-page
│       │   ├── compliance.md         ← Qué NO decir
│       │   ├── source-verification.md← Anti-alucinación
│       │   └── image-guidelines.md   ← Estilo fotográfico y visual
│       ├── briefs/                   ← Briefs generados (YYYY-MM-DD-slug.md)
│       ├── posts/                    ← Posts generados (YYYY-MM-DD-slug.md)
│       └── pipeline/
│           ├── topics-queue.md       ← Keywords en cola
│           ├── status-tracker.md     ← Estado de cada pieza
│           └── content-registry.md   ← Registro de contenido publicado
```
