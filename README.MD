Trabajo realizado por Alberto Rueda, David, Delgado y Daniel Ortiz

# ESCENARIO

La empresa sevillana "Aceites del Aljarafe S.L." opera actualmente con el "Efecto Silo": usan hojas de cálculo para el inventario, una base de datos Access antigua para clientes y facturan a mano. Han contratado a vuestro equipo de consultoría para migrar a un sistema profesional.

# Bloque A: Análisis de Mercado y Selección

Hemos analizado 3 posible soluciones:

## Odoo

### Ventajas:

Es un softare de codigo abierto sin coste de licencias, modular, permite la integracion ventas, usuario,crm... personalizacion y compatible con Docker y PostgreSQL

### Desventajas:

Requiere soporte de mantenimiento y algunas funciones requieren una versiones "enterprise"

## SAP S/4HANA

### Ventajas:

Pontente, alta escabilidad y herramientas de análisis

### Desventajas:

Coste elevado, implantación compleja y excesivo para una empresa de solo 25 empleados

## ZOHO ONE

### Ventajas:

De uso fácil, integración rápida y basado en nube

### Desventajas:

Muy poca capacidad de personalización, dependencia total de proveedor Saas, limitaciones para adaptar procesos

#  ERP Seleccionado

Se selecciona **Odoo Community** como solución ERP para la empresa.

## Justificación de la elección

Odoo Community ofrece el mejor equilibrio entre coste, funcionalidad y flexibilidad para una PYME de 25 empleados.
La empresa necesita:
- Centralizar información.
- Mejorar la gestión de inventario.
- Automatizar facturación.
- Tener capacidad de crecimiento futuro.

Además:
- No tiene coste de licencias.
- Permite personalizar etiquetas y procesos.
- Puede desplegarse en infraestructura cloud económica.
- Facilita futuras ampliaciones mediante módulos.
Por estas razones, Odoo Community es la opción más adecuada

# Cálculo de TCO (Coste Total de Propiedad)

Estimación de costes durante 3 años.
- Licencias Odoo Community  0 € 

- Hosting Cloud  3600 € 

- Implantación (100h × 40 €/h)  4000 € 

- Soporte y mantenimiento  4500 € 

## Coste total estimado

Total a 3 años: 12100 €

# Bloque B: Diseño de Seguridad RBAC

DOCUMENTO PDF

# Bloque C: Documentación de Explotación

## Docker-compose.yml

Documento docker-compose.yml

## comando para realizar un backup de la base de datos PostgreSQL.

bash
docker exec -t nombre_contenedor_db pg_dump -U odoo -F c -b -v -f /backup/odoo_backup.dump postgres


