# content-registry.md — Registro de Contenido Publicado

**Última actualización**: Junio 2026  
**Propósito**: Evitar canibalización. Consultar ANTES de generar cualquier brief.

---

## Instrucciones

Este archivo es la fuente de verdad interna sobre qué contenido existe en el blog de Voltiva.

**Antes de generar un brief**, verificar:
1. ¿Existe un post que ya ataque este keyword primario?
2. ¿Existe un post con intención idéntica aunque el keyword sea diferente?
3. Si hay overlap: ¿es canibalización real o se puede diferenciar la intención?

---

## Inventario de posts publicados

> Sistema recién iniciado — agregar posts a medida que se publiquen

| Slug | Keyword primario | Intención | Fecha | Notas |
|------|-----------------|-----------|-------|-------|
| — | — | — | — | — |

---

## Instrucciones para agregar entradas

Cuando se publique un post, agregar una fila con:

```
| /blog/[slug] | [keyword primario] | [Informacional/Comercial/Transaccional] | [YYYY-MM-DD] | [notas si aplica] |
```

**Ejemplo**:
```
| /blog/cuanto-cuesta-instalar-paneles-solares-colombia | cuanto cuesta instalar paneles solares en colombia | Comercial | 2026-07-01 | Incluye tabla de precios por tipo de sistema |
```

---

## Verificación rápida de canibalización

Para cualquier keyword nuevo, ejecutar mentalmente:

1. **Buscar en este registro** si el keyword o variación cercana ya existe
2. **Buscar en el sitemap live**: `curl -s "https://voltiva.com.co/sitemap.xml" | grep '/blog/'`
3. **Hacer búsqueda**: `site:voltiva.com.co/blog [keyword]`

Si se encuentra match → completar análisis:

```markdown
⚠️ POSIBLE CANIBALIZACIÓN DETECTADA
- Post existente: [URL]
- Keyword existente: [keyword]
- Overlap con nuevo keyword: [describir]
- Recomendación: 
  [ ] Diferenciar intención → proceder con nuevo post
  [ ] Actualizar post existente → no crear nuevo post
  [ ] Fusionar contenidos → reestructurar post existente
  [ ] Descartar nuevo keyword
```
