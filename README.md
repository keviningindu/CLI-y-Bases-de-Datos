# CLI y Bases de Datos - TripleTen Bootcamp

Este proyecto contiene ejercicios prácticos de **línea de comandos (CLI)** y **SQL** realizados durante el Bootcamp de QA Engineer en TripleTen, utilizando **Cygwin64** como entorno de trabajo.

## 🚀 Habilidades adquiridas
- Filtrado de registros en servidores remotos con `grep`
- Creación y organización de directorios en CLI
- Consultas SQL para contar, ordenar y agrupar datos
- Uso de `JOIN` para combinar tablas
- PostgreSQL y Cygwin64

## 📂 Estructura del repositorio
- `logs/` → Ejemplos de registros
- `scripts/` → Comandos CLI
- `sql/` → Consultas SQL
- `docs/` → Documentación del sprint

## 🔎 Ejemplo CLI
```bash
# Buscar todas las solicitudes con código 400 en un archivo de logs
grep -E "400" main.txt > ~/bug1/events/400.txt

## Ejemplo SQL
-- Contar cuántos vehículos únicos tiene cada compañía
SELECT company_name, COUNT(DISTINCT vehicle_id) AS cnt
FROM cabs
GROUP BY company_name
HAVING COUNT(DISTINCT vehicle_id) < 100
ORDER BY cnt DESC;
