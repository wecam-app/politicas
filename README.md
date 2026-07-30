# Políticas — Wecam Leads App

Repositorio de alojamiento de políticas de tratamiento de datos personales para estudios clientes de Wecam Leads App.

**Dominio:** `politicas.tupostulacion.com`
**Servicio:** GitHub Pages, alojamiento técnico. Wecam no revisa ni aprueba el contenido legal de los documentos publicados aquí (ver Anexo C, sección 3.11).

---

## Convención de carpetas

```
[slug-estudio]/v[N]/index.html
```

- `slug-estudio`: minúsculas, sin espacios ni acentos, mismo slug usado en el subdominio de correo de esa subcuenta (ej. `diamante`).
- `v[N]`: número de versión secuencial, empezando en `v1`.

## Regla de oro: nunca se edita una versión publicada

Cuando cambie el contenido de una política:

1. Crear la carpeta `v[N+1]/` con el HTML actualizado.
2. **No tocar** la carpeta de la versión anterior. Debe seguir accesible.
3. Actualizar el Custom Value de la subcuenta en GHL para que apunte a la nueva URL de versión.
4. Registrar el cambio siguiendo el proceso de aprobación (ver más abajo).

## Antes de publicar una carpeta nueva

- [ ] El estudio completó todos los placeholders (`[ESTUDIO_RAZON_SOCIAL]`, `[ESTUDIO_NIT]`, etc.).
- [ ] El estudio confirmó por escrito (correo) que ese es el texto que aprueba publicar.
- [ ] Los puntos marcados "requiere validación legal" fueron revisados o al menos identificados por el estudio.
- [ ] Se eliminaron las secciones que no aplican (documento de identidad, fotografías, etc. si no se usan).
- [ ] El encabezado y el pie llevan el número de versión y la fecha correctos.
- [ ] El banner "EJEMPLO EN VIVO" se eliminó (solo debe existir en `/ejemplo/`).

## Carpeta `/ejemplo/`

Contiene la plantilla de referencia con todos los placeholders visibles, usada para consulta interna y como prueba de la configuración del dominio y GitHub Pages. **No es la política de ningún estudio real y no debe usarse como URL final de ningún cliente.**

## Publicar cambios

```bash
git add [slug-estudio]/v[N]/
git commit -m "Publica política [slug-estudio] v[N]"
git push
```

GitHub Pages actualiza el sitio automáticamente en 1–2 minutos tras el push.
