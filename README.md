# Pipeline de Datos en la Nube - Caso DataCo 
*Integrantes:* 
- Juan Pablo Gallego Valencia  
- Yeferson Grajales  
- Fredy Alberto Licona Mena  
- Manuela Valencia

DataCo es una empresa colombiana dedicada a la distribución de productos de consumo masivo, con operaciones en 12 departamentos del país y más de 9.000 puntos de venta activos entre supermercados, tiendas y droguerías.

La compañía cuenta con aproximadamente:

- 1.800 empleados
- 320 vehículos de distribución
- Tres líneas principales de negocio:
  - Alimentos perecederos
  - Productos de aseo
  - Cosméticos y cuidado personal

Debido al crecimiento de la operación, DataCo ha desarrollado múltiples sistemas independientes para administrar ventas, inventario, logística y relaciones comerciales.

Actualmente la organización opera sobre cuatro sistemas principales:

| Sistema | Tecnología | Función |
|---|---|---|
| ERP de ventas | SAP On-Premise | Facturación y ventas |
| Inventario | Oracle Database | Stock y movimientos |
| GPS flota | Archivos CSV | Rutas y entregas |
| CRM comercial | Salesforce | Clientes y acuerdos |


# Problemática Identificada

La arquitectura tecnológica actual presenta una alta fragmentación de información, debido a que los sistemas operan de manera aislada y sin integración automática.

Esto genera múltiples problemas operativos y estratégicos para la organización.

---

## 1. Procesos manuales de consolidación

El equipo de inteligencia de negocio debe exportar manualmente información desde múltiples plataformas y consolidarla en archivos Excel.

Este proceso tarda entre 3 y 5 días hábiles para generar reportes ejecutivos.

### Impactos

- Retrasos en reportes
- Baja productividad
- Dependencia manual
- Riesgo de errores humanos

---

## 2. Información desactualizada

Los datos de inventario pueden presentar hasta 72 horas de retraso respecto a la operación real.

Esto provoca:

- Quiebres de stock
- Sobreinventario
- Pérdidas económicas
- Mala planeación logística

---

## 3. Inconsistencia de datos

Los productos y clientes presentan diferencias entre sistemas.

Ejemplos:

- Clientes registrados con nombres distintos
- Productos con códigos diferentes
- Formatos inconsistentes de fechas

### Consecuencias

- Dificultad para generar reportes unificados
- Errores analíticos
- Información poco confiable

---

## 4. Falta de trazabilidad logística

No existe una correlación automática entre:

- Facturas SAP
- Entregas GPS
- Rutas comerciales
- Cumplimiento logístico

Esto impide medir:

- Tiempo real de entrega
- Cumplimiento por vendedor
- Eficiencia de rutas

---
## 5. Problemas de escalabilidad

El procesamiento actual depende de un servidor Windows Server 2012 con capacidad limitada.

Durante temporadas de alta demanda:

- Los reportes tardan hasta 8 horas
- El sistema presenta degradación de rendimiento
- Existen riesgos de indisponibilidad

---
