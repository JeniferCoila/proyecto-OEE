# Plataforma de Monitoreo OEE

## Resumen

El presente proyecto busca desarrollar una plataforma para el monitoreo y mejora del **Overall Equipment Effectiveness (OEE)**, permitiendo a las empresas manufactureras optimizar sus procesos productivos. El enfoque inicial incluye la creación de una aplicación web dinámica utilizando **Java** y tecnologías relacionadas.

## Marco Teórico

El **OEE (Overall Equipment Effectiveness)** es una métrica clave que mide la eficiencia en las líneas de producción considerando tres factores:
1. **Disponibilidad:** Tiempo efectivo de operación respecto al planificado.
2. **Rendimiento:** Velocidad real de producción en comparación con la capacidad máxima.
3. **Calidad:** Porcentaje de productos sin defectos.

El objetivo de esta métrica es identificar áreas de mejora y maximizar la productividad.

## Objetivo del Proyecto

Desarrollar una aplicación web dinámica que permita medir y visualizar el OEE en tiempo real, enfocándose en la accesibilidad de datos y la facilidad de uso para operadores y gerentes.

## Tecnologías Utilizadas

- **Lenguaje:** Java (Dynamic Web Project)
- **Base de Datos:** MySQL
- **Servidor de Aplicaciones:** Apache Tomcat 9.0
- **Editor de Código:** Eclipse IDE for Enterprise Java Developers
- **Arquitectura:** Desarrollo inicial sin backend (lógica implementada en Java y JSP)

## Instalación y Configuración

1. **Configuración del entorno de desarrollo:**
   - Descarga e instala **Eclipse IDE for Enterprise Java Developers**.
   - Configura el servidor **Apache Tomcat 9.0** en Eclipse:
     - Ve a `Window > Preferences > Server > Runtime Environments`.
     - Añade **Apache Tomcat 9.0** y configura el directorio de instalación.

2. **Configuración de la base de datos:**
   - Instala y configura **MySQL Server**.
   - Crea una base de datos llamada `oee_monitoring`:
     ```sql
     CREATE DATABASE oee_monitoring;
     ```
   - Crea las tablas necesarias (ejemplo básico):
     ```sql
     CREATE TABLE production_data (
         id INT AUTO_INCREMENT PRIMARY KEY,
         equipment_id VARCHAR(50),
         availability DECIMAL(5, 2),
         performance DECIMAL(5, 2),
         quality DECIMAL(5, 2),
         timestamp DATETIME DEFAULT CURRENT_TIMESTAMP
     );
     ```

3. **Importación del proyecto en Eclipse:**
   - Descarga el código del repositorio y descomprímelo.
   - En Eclipse, ve a `File > Import > Existing Projects into Workspace`.
   - Selecciona la carpeta del proyecto.

4. **Ejecución de la aplicación:**
   - Inicia el servidor Tomcat en Eclipse.
   - Abre un navegador y accede a `http://localhost:8080/nombre_proyecto`.

## Funcionalidades Básicas

- **Captura de datos:** Registro manual de datos de disponibilidad, rendimiento y calidad.
- **Visualización:** Cálculo y despliegue del OEE en tablas simples.
- **Interfaz inicial:** Diseñada con HTML, CSS y JSP.

## Futuras Mejoras

- Implementar un backend para lógica de negocio avanzada.
- Desarrollar gráficos interactivos para visualizar tendencias del OEE.
- Añadir funcionalidades de mantenimiento preventivo y alertas automáticas.

