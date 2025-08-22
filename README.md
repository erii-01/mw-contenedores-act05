# Actividad 05 - Docker Compose

Este repositorio contiene las actividades prácticas relacionadas con Docker Compose y contenedorización de aplicaciones web.

## Estructura del Proyecto

### 📁 act05-02/
**Servidor web básico con Docker Compose**
- `docker-compose.yml`: Configuración para servidor web Nginx
- `web/index.html`: Página web estática de ejemplo
- **Propósito**: Demostrar el uso básico de Docker Compose con un servidor web simple

### 📁 act05-03/
**Configuración avanzada de servicios**
- `docker-compose.yml`: Configuración multi-servicio
- **Propósito**: Explorar configuraciones más complejas de Docker Compose

### 📁 act05-04/
**Servidor web con configuración personalizada**
- `docker-compose.yml`: Configuración de Nginx personalizado
- `nginx.conf`: Archivo de configuración personalizado para Nginx
- **Propósito**: Demostrar el uso de archivos de configuración externos

### 📁 act05-05/
**Aplicación con imagen personalizada**
- `Dockerfile`: Definición de imagen personalizada
- `docker-compose.yml`: Orquestación de servicios
- `configuration.yml`: Archivo de configuración de la aplicación
- **Propósito**: Integrar imágenes personalizadas con Docker Compose

### 📁 act05-06/mikroways.net/
**Sitio web Hugo en contenedores para desarrollo**
- **Sitio web completo**: Sitio corporativo de Mikroways desarrollado con Hugo
- `docker-compose.yml`: Entorno de desarrollo containerizado
- `config.toml`: Configuración del sitio Hugo
- `content/`: Contenido del sitio en inglés y español
- `layouts/`: Plantillas y layouts personalizados
- `static/`: Archivos estáticos (CSS, JS, imágenes)
- `themes/`: Tema Hugo personalizado
- **Propósito**: Entorno de desarrollo completo sin instalación local de Hugo

## Uso

### Para cualquier actividad específica:
```bash
cd act05-XX/
docker-compose up -d
```

### Para el sitio Hugo (act05-06):
```bash
cd act05-06/mikroways.net/
docker-compose up -d
# Acceder a: http://localhost:1313
```

## Características del Entorno de Desarrollo Hugo

- **Hot Reload**: Los cambios se reflejan automáticamente en el navegador
- **Sin instalación local**: No requiere Hugo instalado en la máquina local
- **Desarrollo completo**: Soporte para borradores y modo desarrollo
- **Versionado local**: Todos los cambios se realizan en archivos locales

## Tecnologías Utilizadas

- **Docker**: Contenedorización de aplicaciones
- **Docker Compose**: Orquestación de servicios
- **Nginx**: Servidor web
- **Hugo**: Generador de sitios estáticos
- **HTML/CSS/JavaScript**: Frontend

## Requisitos

- Docker
- Docker Compose

## Comandos Útiles

```bash
# Iniciar servicios
docker-compose up -d

# Ver logs
docker-compose logs

# Detener servicios
docker-compose down

# Reconstruir imágenes
docker-compose build --no-cache

# Ver estado de contenedores
docker-compose ps
```