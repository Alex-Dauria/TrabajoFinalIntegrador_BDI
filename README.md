# Trabajo Final Integrador - Bases de Datos I  
## Sistema de Gestión de Empleados  

### 👥 Integrantes del Grupo 2 
- **Giardini Silvia** - Comisión 07  
- **Marina Giselle Cordero** - Comisión 07  
- **Alex Dauria** - Comisión 06  
- **Matías Perdigués** - Comisión 01  

### 🎓 Profesores  
- **Nicolás Carcaño** - Comisión 07  
- **Verónica Tomich** - Comisión 06  
- **Guillermo Londero** - Comisión 01  

---

## 🎥 Video Explicativo  
[Enlace al Video](https://youtu.be/ejemplo-video-tfi)  

---

## 📋 Descripción del Proyecto  
Este Trabajo Final Integrador implementa un sistema completo de **gestión de empleados** utilizando MySQL, abarcando desde el modelado conceptual hasta la gestión de concurrencia avanzada. El proyecto simula un entorno real con más de 450,000 registros y aborda todos los aspectos fundamentales de las bases de datos relacionales.

---

## 🏗️ Arquitectura del Sistema  

### Modelo de Datos
- **2 entidades principales**: Empleados y Legajos
- **Relación 1:1** entre empleados y sus legajos
- **Constraints completos**: PK, FK, UNIQUE, CHECK, ENUM
- **Validación de dominio** para emails, fechas y estados

### Tecnologías Utilizadas
- **SGBD**: MySQL 8.0+
- **Lenguaje**: SQL estándar
- **Características avanzadas**: Transacciones, Vistas, Procedimientos almacenados

---

## 📁 Estructura del Repositorio

### Archivos en la raíz:
- `README.md` - Este archivo
- `TFI_BDI_Comisiones1,6,7_Grupo2_Cordero_Dauria_Giardini_Perdigues.pdf` - Documentación principal
- `TFI_BDI_IA_Complementario_Comisiones1,6,7_Grupo2_Cordero_Dauria_Giardini_Perdigues.pdf` - Interacciones con herramientas de IA
- `TFI_BDI_Comisiones1,6,7_Grupo2_Cordero_Dauria_Giardini_Perdigues.zip` - Scripts SQL comprimidos

### Contenido del ZIP:
| Archivo | Descripción |
|---------|-------------|
| `01_esquema.sql` | Creación de BD, tablas y constraints |
| `02_catalogos.sql` | Estructura de catálogos (vacío en este diseño) |
| `03_datos_masivos.sql` | Generación de 450,000 registros |
| `04_indices.sql` | Creación y verificación de índices |
| `05_consultas.sql` | 4 consultas avanzadas con análisis |
| `05_explain.sql` | Medición de rendimiento con/sin índices |
| `06_vistas.sql` | Vistas para reportes ejecutivos |
| `07_seguridad.sql` | Usuarios, permisos y procedimientos seguros |
| `08_transacciones.sql` | Manejo de transacciones y concurrencia |
| `09_concurrencia-guiada.sql` | Pruebas guiadas de concurrencia |

---

## 🚀 Instalación y Ejecución

### Prerrequisitos
- MySQL Server 8.0 o superior
- Cliente MySQL (MySQL Workbench recomendado)

### Pasos de Implementación
1. **Descargar y descomprimir los scripts**
   - Descargar `TFI_BDI_ComisionX_Grupo2_Cordero_Dauria_Giardini_Perdigues.zip`
   - Extraer todos los scripts SQL en una carpeta

2. **Ejecutar scripts en orden**:
   ```sql
   -- 1. Esquema base
   SOURCE 01_esquema.sql;
   
   -- 2. Datos masivos (aproximadamente 450,000 registros)
   SOURCE 03_datos_masivos.sql;
   
   -- 3. Optimización
   SOURCE 04_indices.sql;
   
   -- 4. Consultas y vistas
   SOURCE 05_consultas.sql;
   SOURCE 06_vistas.sql;
   
   -- 5. Seguridad
   SOURCE 07_seguridad.sql;
   
   -- 6. Concurrencia
   SOURCE 08_transacciones.sql;
   SOURCE 09_concurrencia-guiada.sql;

---

## 📊 Características Destacadas

### ✅ Etapa 1 - Modelado
- DER con 2 entidades y relación 1:1
- Constraints completos (PK, FK, UNIQUE, CHECK)
- Validación práctica con inserciones válidas/erróneas

### 📈 Etapa 2 - Datos Masivos
- **450,000 empleados** y **450,000 legajos** generados
- Distribución equilibrada por áreas (≈20% cada una)
- Integridad referencial garantizada (0 FK huérfanas)

### 🔍 Etapa 3 - Consultas Avanzadas
- 4 consultas complejas con JOIN, GROUP BY, HAVING, subconsultas
- 2 vistas estratégicas para reportes ejecutivos
- **Análisis de rendimiento**: índices mejoraron JOINs 2.34x y rangos 3.93x

### 🔒 Etapa 4 - Seguridad
- Usuario con **mínimos privilegios** (`gerente_marketing`)
- Vistas con `WITH CHECK OPTION` para acceso restringido
- Procedimiento almacenado **resistente a SQL Injection**

### ⚡ Etapa 5 - Concurrencia
- Pruebas de **deadlock** y **timeout**
- Comparación de niveles de aislamiento (READ COMMITTED vs REPEATABLE READ)
- Procedimiento con **retry automático** ante deadlocks

---


## 🧠 Aprendizajes Clave

1. **Los índices son cruciales** para consultas de rango y JOINs complejos
2. **REPEATABLE READ** ofrece mayor consistencia que READ COMMITTED
3. **Las vistas con CHECK OPTION** son efectivas para seguridad por fila
4. **El retry automático** es esencial para manejar deadlocks en producción
5. **La generación masiva de datos** requiere planificación para mantener integridad

---

## 🔗 Enlaces

- **Repositorio**: [https://github.com/Alex-Dauria/TrabajoFinalIntegrador_BDI](https://github.com/Alex-Dauria/TrabajoFinalIntegrador_BDI)
- **Video Explicativo**: [https://youtu.be/ejemplo-video-tfi](https://youtu.be/ejemplo-video-tfi)

---

*Este trabajo fue desarrollado como parte de la materia Bases de Datos I de la Tecnicatura Universitaria en Programación a Distancia, aplicando mejores prácticas y uso responsable de herramientas de IA como apoyo pedagógico.*
