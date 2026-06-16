# source-verification.md — Protocolo Anti-Alucinación

**Versión**: 1.0  
**Última actualización**: Junio 2026

---

## Propósito

Este protocolo existe para evitar que el agente invente datos, URLs, estadísticas, estudios o afirmaciones que no existen. En el sector de energía solar, datos incorrectos pueden generar expectativas irreales en clientes y dañar la credibilidad de Voltiva.

**Regla principal: Si no puedes verificarlo, no lo incluyas. Si lo incluyes, marca la fuente.**

---

## Tipos de contenido y su protocolo de verificación

### 1. Datos estadísticos y cifras de mercado
**Protocolo**:
- Solo usar cifras de fuentes verificadas: UPME, IDEAM, IRENA, Banco Mundial, Ministerio de Minas
- Si tienes una cifra aproximada pero no la fuente exacta: usar "aproximadamente" o "según reportes del sector" y buscar la fuente real
- Si no encuentras la fuente: **no incluir la cifra**

**Fuentes confiables para datos solares en Colombia**:
| Dato | Fuente recomendada |
|------|-------------------|
| Irradiación solar por región | IDEAM — Atlas de Radiación Solar |
| Capacidad instalada en Colombia | UPME — Informes de energías renovables |
| Número de proyectos registrados | UPME — FENOGE |
| Marco regulatorio | CREG — creg.gov.co |
| Datos globales de solar | IRENA — irena.org |
| Tendencias de precios de paneles | BloombergNEF, IRENA |

---

### 2. URLs y links
**Protocolo**:
- **NUNCA inventar URLs** de voltiva.com.co
- Antes de incluir cualquier link interno, verificar que existe haciendo fetch de la URL
- Para links externos, usar solo dominios oficiales (.gov.co, .org, publicaciones académicas)
- Si un link no existe, NO incluirlo en el post

**Verificación de URLs internas**:
```bash
# Verificar que una URL de Voltiva existe antes de linkear
curl -s -o /dev/null -w "%{http_code}" "https://voltiva.com.co/[ruta]"
# Si devuelve 200: link válido
# Si devuelve 404 o 301: no incluir o verificar redirección
```

---

### 3. Análisis SERP
**Protocolo**:
- Usar web_search para obtener datos SERP reales, no inventados
- Si no puedes verificar posiciones, word counts o URLs de competidores: marcar como `[requiere verificación manual]`
- Nunca inventar contenido de artículos competidores

---

### 4. Estudios científicos o técnicos
**Protocolo**:
- Solo citar estudios que puedas verificar (autor, año, publicación)
- No inventar instituciones, universidades o investigaciones
- Si quieres decir "un estudio dice X": primero busca el estudio real, si no lo encuentras, reformula sin citar estudio

---

### 5. Datos de Voltiva (proof points de la empresa)
**Estos datos son verificados y aprobados por el equipo Voltiva**:
- +34 proyectos instalados ✅
- +400 kWp instalados en Colombia ✅
- Monitoreo 24/7 ✅
- Financiación sin cuota inicial ✅
- Sistema diseñado a la medida ✅
- Equipos de máxima calidad ✅

**NUNCA inventar datos nuevos de Voltiva** sin aprobación del equipo.

---

## Señales de alerta: cuándo detener y verificar

El agente debe pausar y verificar (o marcar para verificación humana) cuando:

1. Va a incluir una cifra específica sin tener la fuente a mano
2. Va a incluir una URL que no ha verificado existe
3. Va a afirmar algo sobre la regulación colombiana sin citar el artículo exacto
4. Va a describir el contenido de un artículo competidor que no ha leído
5. Va a citar un estudio o investigación específica

---

## Marcadores de incertidumbre aprobados

Cuando algo no está verificado pero es razonable incluirlo con advertencia:

```markdown
[VERIFICAR: este dato requiere confirmación con fuente oficial antes de publicar]
[DATO APROXIMADO: basado en estimaciones del sector, verificar con UPME]
[LINK PENDIENTE: agregar URL real de voltiva.com.co/[ruta] antes de publicar]
[ACTUALIZAR: verificar si esta regulación sigue vigente en 2026]
```

---

## Checklist de verificación de fuentes

Completar antes de entregar cualquier brief o post:

- [ ] Datos del SERP basados en búsqueda web real (no inventados)
- [ ] URLs de competidores verificadas (existen y el contenido es el descrito)
- [ ] Estadísticas tienen fuente citada y verificable
- [ ] Links internos a voltiva.com.co verificados (HTTP 200)
- [ ] Links externos a fuentes de alta autoridad
- [ ] Afirmaciones regulatorias con artículo/ley específico verificado
- [ ] Proof points de Voltiva son los aprobados (no inventados)
- [ ] No hay estudios o investigaciones inventadas
