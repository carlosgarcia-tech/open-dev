# Política de seguridad OpenDev

## Cómo reportar una vulnerabilidad

No publiques detalles de seguridad en issues, discussions ni Pull Requests públicos.

Usa el reporte privado de vulnerabilidades de GitHub:

1. Abre la pestaña **Security** del repositorio.
2. Entra en **Advisories**.
3. Pulsa **Report a vulnerability**.

También puedes contactar directamente con el maintainer indicado en el perfil del repositorio.

Incluye, si es posible:

- Descripción del problema.
- Pasos para reproducirlo.
- Impacto potencial.
- Versión de Java y sistema operativo.
- Cualquier prueba de concepto, sin datos sensibles.

## Qué esperar

- Confirmaremos la recepción del reporte lo antes posible.
- Investigaremos y mantendremos informada a la persona que reporta.
- Si la vulnerabilidad se confirma, prepararemos una corrección y coordinaremos la divulgación.
- No prometemos plazos de respuesta concretos, pero trataremos los reportes de seguridad con prioridad.

## Alcance

Este repositorio es educativo y no contiene servicios en producción ni datos de usuarios. Aun así, nos importan:

- La seguridad de las dependencias de Maven.
- La configuración de GitHub Actions.
- Cualquier riesgo de ejecución de código no confiable.

## Buenas prácticas para contribuir

- No incluyas secretos, tokens ni contraseñas en el repositorio.
- No ejecutes código de Pull Requests de forks sin revisarlo.
- No uses `pull_request_target` para ejecutar código no confiable.
- Mantén las dependencias actualizadas y revisa los avisos de Dependabot.

## Divulgación responsable

Pedimos que no se divulgue públicamente una vulnerabilidad hasta que exista una corrección o se acuerde una fecha de publicación. Agradecemos la colaboración de quienes ayudan a mantener el proyecto seguro.
