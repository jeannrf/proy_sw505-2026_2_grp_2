# SiMuLiF

**Sistema Municipal de Licencias de Funcionamiento**, proyecto 4 del curso SW505 Proceso de Construcción de Software I (ciclo 2026-2), grupo 2.

## ¿Qué es SiMuLiF?

Es una aplicación web que simula cómo una municipalidad distrital del Perú atiende el trámite de licencia de funcionamiento, de principio a fin y sin papeles.

El recorrido de un expediente es el siguiente:

- **Registro.** El solicitante, sea persona natural o empresa, registra su local y su giro. El sistema le indica el nivel de riesgo y la lista de requisitos que debe cumplir.
- **Presentación.** Adjunta sus documentos, paga el derecho de trámite (pago simulado) y envía la solicitud.
- **Evaluación.** Mesa de partes revisa los requisitos y el evaluador verifica la zonificación. Si el riesgo es alto o muy alto, un inspector realiza la ITSE antes de emitir la licencia. Si hay observaciones, el solicitante las subsana dentro del plazo.
- **Resultado.** El jefe de licencias aprueba o deniega. Si se aprueba, se genera la licencia en PDF con un código QR que cualquier persona puede verificar en línea.

Es un trabajo académico: no pertenece a ninguna municipalidad, y los plazos, montos y servicios externos (RENIEC, SUNAT, pagos) son simulados.

## ¿Qué mejora?

- **Para el ciudadano:** no tiene que ir a ventanilla, conoce los requisitos desde el primer momento y puede ver en línea en qué etapa está su trámite.
- **Para la municipalidad:** cada funcionario tiene su bandeja de trabajo, los plazos en días hábiles se controlan solos y llegan menos expedientes incompletos.
- **Para la transparencia:** cada acción sobre un expediente queda registrada, el estado del trámite se puede consultar públicamente y las licencias se validan con el QR.

## Equipo

Los tres integrantes desarrollamos como full stack. La división es por documentos de la fase 1, y cada uno es responsable de los suyos.

| Integrante | Rol | Documentos a cargo |
|---|---|---|
| Luis Bustamante Rojas | Desarrollador full stack, responsable de requerimientos y análisis | 1, 2 y 3 |
| Jose Antonio Arredondo Tomairo | Desarrollador full stack, responsable de modelo lógico, casos de uso del sistema y planificación | 4, 5 y 8 |
| Jeanpier Alexander Robles Fabian | Desarrollador full stack, responsable de base de datos, arquitectura y despliegue | 6, 7 y 9 |

El docente del curso tiene acceso al repositorio como colaborador.

## Documentos

Todo está en la carpeta [`Documentos`](Documentos).

**[Análisis y diseño](<Documentos/analisis_y_diseño>)**, entregado en la fase 1 (12/11/2026):

1. [Requerimientos funcionales](<Documentos/analisis_y_diseño/1. Requerimientos funcionales.md>): alcance, usuarios y los 45 requerimientos funcionales.
2. [Requerimientos no funcionales](<Documentos/analisis_y_diseño/2. Requerimientos no funcionales.md>): restricciones, supuestos, interfaces y 18 requerimientos de calidad.
3. [Análisis: casos de uso del negocio](<Documentos/analisis_y_diseño/3. Analisis - Casos de uso del negocio.md>): marco normativo, actores, procesos del negocio y reglas de negocio.
4. [Modelo lógico de datos](<Documentos/analisis_y_diseño/4. Modelo lógico de datos.md>): diagrama entidad-relación, diccionario de datos y modelo documental.
5. [Diseño: casos de uso del sistema](<Documentos/analisis_y_diseño/5. Diseño - Casos de uso del sistema.md>): 20 casos de uso, estados del expediente y trazabilidad.
6. [Modelo físico de datos](<Documentos/analisis_y_diseño/6. Modelo físico de datos.md>): tablas en PostgreSQL, colecciones en MongoDB y buckets en MinIO, con sus scripts.
7. [Diseño de arquitectura](<Documentos/analisis_y_diseño/7. Diseño de arquitectura.md>): las 7 capas, componentes, API, seguridad y despliegue.

**[Implementación y despliegue](<Documentos/implementacion_y_despliegue>)**:

8. [Plan de implementación](<Documentos/implementacion_y_despliegue/8. Plan de implementación.md>): incrementos semanales, reparto de tareas, flujo de trabajo en Git y riesgos.
9. [Guía de despliegue y operaciones](<Documentos/implementacion_y_despliegue/9. Guía de despliegue y operaciones.md>): instalación con Docker, configuración, respaldos y solución de problemas.

Para la fase 2 se suman el plan y los resultados de pruebas y la documentación del código.

## Stack

- **Frontend:** React 18 con TypeScript y Vite.
- **Backend:** Python 3.12 con FastAPI.
- **Datos:** PostgreSQL 16 para la información del trámite, MongoDB 7 para observaciones, inspecciones y bitácora, y MinIO para los archivos.
- **Seguridad:** Nginx con HTTPS como única entrada, autenticación con JWT y permisos por rol.
- **Infraestructura:** Docker Compose y GitHub Actions.

## Organización del repositorio

```
proy_sw505-2026_2_grp_2/
├── README.md
└── Documentos/
    ├── analisis_y_diseño/            documentos 1 al 7
    └── implementacion_y_despliegue/  documentos 8 y 9
```

El código (`backend/`, `frontend/`, `database/` y `deploy/`) se agrega durante la fase 2.

## Fechas clave

| Fecha | Qué se entrega |
|---|---|
| 12/11/2026 | Fase 1: exposición del análisis y diseño |
| 19/11/2026 | Incremento 1: base técnica, inicio de sesión, registro y cálculo de riesgo |
| 26/11/2026 | Incremento 2: presentación, verificación, zonificación y observaciones |
| 03/12/2026 | Incremento 3 y fase 2: inspección, decisión, licencia con QR y sistema desplegado |
