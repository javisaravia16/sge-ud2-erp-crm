# Comparativa ERP y CRM

## 1. Datos
* **Propietario:** javisaravia16
* **Empresa:** 4 - Startup SaaS
* **Palabra del día:** Integración

## 2. Licencias y modelos
La diferencia principal radica en que el software libre (FSF) prioriza la libertad ética y moral del usuario, el código abierto (OSI) se enfoca en la eficiencia práctica del desarrollo colaborativo, y el software propietario restringe totalmente el acceso y control bajo una empresa o dueño.  

El software libre define derechos de uso y modificación, no su precio, mientras que el modelo Community frente a Enterprise representa una estrategia comercial para rentabilizar dicho software.


## 3. Fichas técnicas

### ERP Libre: Odoo Community
* **Licencia:** LGPLv3
* **Versión vigente:** Odoo 17 
* **Lenguaje del servidor:** Python
* **SGBD compatibles:** PostgreSQL.
* **Modalidad:** Instalación local / Hosting propio
* **Módulos principales:** Ventas, CRM, Inventario, Facturación básica (la contabilidad avanzada es Enterprise).
* **Requisitos:** Servidor Linux/Windows, Python 3.10+, PostgreSQL 12+.
* **Fuente:** [Odoo Editions](https://www.odoo.com/) (Consultado: 23/09/2026)

### ERP Propietario: Microsoft Dynamics 365
* **Licencia:** Propietaria (Suscripción SaaS).
* **Versión vigente:** Dynamics 365 2026 Release Wave.
* **Lenguaje del servidor:** C# / .NET.
* **SGBD compatibles:** Microsoft SQL Server / Azure SQL.
* **Modalidad:** Principalmente Nube (Azure).
* **Módulos principales:** Finanzas, Cadena de suministro, Ventas, RRHH.
* **Requisitos:** Navegador web moderno, conexión a internet, Azure AD.
* **Fuente:** [Microsoft Learn](https://learn.microsoft.com/es-es/dynamics365/) (Consultado: 23/09/2026).

### CRM Libre: SuiteCRM
* **Licencia:** AGPLv3.
* **Versión vigente:** SuiteCRM 8.x.
* **Lenguaje del servidor:** PHP.
* **SGBD compatibles:** MySQL, MariaDB.
* **Modalidad:** Local / Nube.
* **Módulos principales:** Cuentas, Contactos, Oportunidades, Campañas.
* **Requisitos:** Apache/Nginx, PHP 8+, MySQL/MariaDB.
* **Fuente:** [SuiteCRM Docs](https://docs.suitecrm.com/) (Consultado: 23/09/2026).

### CRM Propietario: Salesforce
* **Licencia:** Propietaria (SaaS).
* **Versión vigente:** Winter '26 (o actual).
* **Lenguaje del servidor:** Apex (propietario basado en Java).
* **SGBD compatibles:** Base de datos propietaria nativa (Oracle bajo el capó).
* **Modalidad:** Exclusivamente Nube.
* **Módulos principales:** Sales Cloud, Service Cloud, Marketing Cloud.
* **Requisitos:** Navegador web.
* **Fuente:** [Salesforce Releases](https://help.salesforce.com/) (Consultado: 23/09/2026).

## 4. Fe de erratas del tema 2

### - Versión actual de Odoo e incoherencia con los requisitos de Python
* **Qué dice el tema:** En la página 7 (apartado 6, «ERP libre»), el texto indica que en Odoo *«su versión actual es la 14»* y añade a continuación que *«requiere la versión 3.10 o posterior de Python»* (escribiendo además «Phyton» de forma errónea).
* **Qué es correcto hoy:** 
  1. Odoo 14 es una versión desactualizada lanzada en 2020; las versiones vigentes y estables actuales son Odoo 17 y Odoo 18.
  2. Existe una incoherencia técnica en el propio texto: Odoo 14 utilizaba entornos Python 3.6 a 3.8. El soporte y requisito obligatorio para Python 3.10 no llegó hasta el lanzamiento de Odoo 16 (a finales de 2022).
* **Fuente:** Repositorio oficial de Odoo en GitHub (`https://github.com/odoo/odoo`) y notas oficiales de lanzamiento de versiones de Odoo.

### - Versión y arquitectura vigente de SuiteCRM
* **Qué dice el tema:** En la página 8 (apartado 8, «CRM libre»), se afirma sobre SuiteCRM que *«Su código fuente y documentación están disponibles en GitHub con una versión (7.14.5) de código abierto bajo licencia AGPL-3.0»*.
* **Qué es correcto hoy:** La rama SuiteCRM 7.x llegó a su fin de ciclo de soporte (End of Life). La versión principal y vigente es **SuiteCRM 8** (SuiteCRM 8.x), la cual introdujo una reescritura arquitectónica profunda adoptando Symfony para el backend y una interfaz basada en Angular.
* **Fuente:** Documentación oficial y repositorio de SalesAgility (`https://docs.suitecrm.com/` y `https://github.com/salesagility/SuiteCRM-Core`).

## 5. Matriz de decisión y recomendación

* **Empresa 4 (Startup SaaS):** 12 empleados, técnicos en Python, presupuesto ajustado al principio pero con crecimiento rápido y facturación por suscripción.

**Justificación de puntuaciones:**
* *Coste:* Odoo Community recibe un 5 por no tener coste de licencia, vital para los 12 empleados iniciales. Salesforce y Dynamics penalizan por su alto coste por usuario.
* *Integración con Python:* Odoo está escrito en Python, lo que permite al equipo técnico de la Startup integrarlo o crear módulos nativamente (5). Salesforce (API REST buena) un 4.
* *Suscripciones:* Salesforce gestiona esto impecablemente de forma nativa (5).
* *Puntuación Ponderada Estimada:* Odoo (4.15), Salesforce (3.85), Dynamics 365 (3.25).

**Recomendación final:** 
Recomiendo **Odoo (versión Community o escalar a Enterprise si es necesario)**. Al ser un equipo de 12 personas que programan en Python, tendrán autonomía para alojar y mantener Odoo, adaptándolo a su facturación por suscripción usando código abierto. 

**Riesgos:**
* **Coste Total (TCO):** Aunque la licencia es gratis, el mantenimiento recae en el equipo técnico.
* **Migración:** Si la startup crece exponencialmente, migrar los datos de Odoo Community a una solución superior puede ser complejo.
* **Soporte:** No hay soporte oficial, dependerán de foros comunitarios.