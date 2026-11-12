# SiMuLiF: Sistema Municipal de Licencias de Funcionamiento de Establecimientos Comerciales

Curso SW505 Construcción de Software I, ciclo 2026-2, grupo 2 (proyecto 4).

## Descripción del proyecto

SiMuLiF es una aplicación web que gestiona el ciclo completo de una solicitud de licencia de funcionamiento en una municipalidad distrital del Perú. El ciudadano hace todo el trámite en línea y cada área de la municipalidad atiende su parte desde el sistema.

El sistema cubre estas etapas:

1. **Registro** del solicitante (persona natural o jurídica con su representante) y de su establecimiento, con la actividad económica que va a desarrollar.
2. **Cálculo del nivel de riesgo** del local y de los requisitos que le corresponden.
3. **Presentación del expediente** con los documentos digitales y el pago del derecho de trámite.
4. **Validación de requisitos** por mesa de partes.
5. **Evaluación de zonificación y compatibilidad de uso** del giro en la zona del predio.
6. **Inspección técnica de seguridad (ITSE)** antes de otorgar la licencia, cuando el riesgo es alto o muy alto.
7. **Observaciones y subsanaciones** dentro de plazos contados en días hábiles.
8. **Decisión y emisión** de la licencia en PDF con código QR verificable, o de la resolución de denegatoria.
9. **Consulta del estado** del trámite por el solicitante y consulta pública por cualquier persona.

Se basa en la Ley N.° 28976, Ley Marco de Licencia de Funcionamiento, y en el Reglamento de ITSE (D.S. N.° 002-2018-PCM). Es un producto mínimo viable con fines académicos: la licencia, el pago, las notificaciones y las consultas a RENIEC y SUNAT son simulados.

**Tecnologías:** React con TypeScript (frontend), Python con FastAPI (backend), PostgreSQL, MongoDB y MinIO (datos y archivos), Nginx (seguridad y entrada), Docker Compose (despliegue).

## Beneficios de la aplicación

- **Reduce los tiempos de atención.** El ciudadano presenta su solicitud en línea, sin hacer colas en ventanilla, y cada funcionario tiene su bandeja con los expedientes que le tocan.
- **Estandariza los requisitos por procedimiento.** El sistema calcula qué requisitos aplican según el nivel de riesgo y el tipo de solicitante, y no permite presentar un expediente incompleto.
- **Da trazabilidad y auditoría de cada expediente.** Cada acción queda registrada con su fecha, su usuario y su resultado, y ese registro no se puede modificar.
- **Permite al ciudadano conocer el estado de su trámite.** Puede consultarlo en cualquier momento y recibe una notificación cada vez que el expediente cambia de etapa.
- **Controla los plazos legales.** Cuenta días hábiles, alerta antes de los vencimientos y aplica el abandono o el silencio administrativo positivo cuando corresponde.
- **Hace verificable la licencia.** Cualquier persona puede escanear el QR de la licencia y confirmar que es auténtica y está vigente.

## Integrantes

| Integrante | Rol en el proyecto | Documentos a cargo |
|---|---|---|
| Luis Bustamante Rojas | Desarrollador full stack, responsable del análisis de requerimientos y de los casos de uso del negocio | 1. Requerimientos funcionales<br>2. Requerimientos no funcionales<br>3. Análisis: casos de uso del negocio |
| Jose Antonio Arredondo Tomairo | Desarrollador full stack, responsable del modelo lógico, los casos de uso del sistema y la planificación | 4. Modelo lógico de datos<br>5. Diseño: casos de uso del sistema<br>8. Plan de implementación |
| Jeanpier Alexander Robles Fabian | Desarrollador full stack, responsable de la base de datos, la arquitectura y el despliegue | 6. Modelo físico de datos<br>7. Diseño de arquitectura<br>9. Guía de despliegue y operaciones |

## Documentación

Los entregables están en la carpeta [`Documentos`](Documentos):

- [`analisis_y_diseño`](<Documentos/analisis_y_diseño>): documentos 1 al 7, de la exposición del 12/11/2026.
  - [1. Requerimientos funcionales](<Documentos/analisis_y_diseño/1. Requerimientos funcionales.md>)
  - [2. Requerimientos no funcionales](<Documentos/analisis_y_diseño/2. Requerimientos no funcionales.md>)
  - [3. Análisis: casos de uso del negocio](<Documentos/analisis_y_diseño/3. Analisis - Casos de uso del negocio.md>)
  - [4. Modelo lógico de datos](<Documentos/analisis_y_diseño/4. Modelo lógico de datos.md>)
  - [5. Diseño: casos de uso del sistema](<Documentos/analisis_y_diseño/5. Diseño - Casos de uso del sistema.md>)
  - [6. Modelo físico de datos](<Documentos/analisis_y_diseño/6. Modelo físico de datos.md>)
  - [7. Diseño de arquitectura](<Documentos/analisis_y_diseño/7. Diseño de arquitectura.md>)
- [`implementacion_y_despliegue`](<Documentos/implementacion_y_despliegue>): documentos 8 y 9.
  - [8. Plan de implementación](<Documentos/implementacion_y_despliegue/8. Plan de implementación.md>)
  - [9. Guía de despliegue y operaciones](<Documentos/implementacion_y_despliegue/9. Guía de despliegue y operaciones.md>)
