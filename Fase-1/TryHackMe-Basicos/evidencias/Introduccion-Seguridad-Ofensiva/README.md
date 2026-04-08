# Introducción a la Seguridad Ofensiva – TryHackMe

## Objetivo
Comprender los fundamentos de la seguridad ofensiva y cómo un analista o pentester puede identificar funcionalidades expuestas dentro de una aplicación web en un entorno controlado.

---

## ¿Qué es la seguridad ofensiva?
La seguridad ofensiva consiste en pensar y actuar como un atacante ético para descubrir debilidades, errores de configuración o fallas de seguridad antes de que sean aprovechadas por actores maliciosos.

Su objetivo no es dañar sistemas, sino *identificar vulnerabilidades de forma autorizada* para fortalecer la seguridad.

---

## Conceptos aprendidos

### Seguridad ofensiva
Área de la ciberseguridad enfocada en detectar vulnerabilidades mediante pruebas controladas.

### Hacking ético
Práctica de evaluar sistemas con autorización para identificar fallas de seguridad.

### Enumeración web
Proceso de descubrir rutas, páginas o directorios ocultos dentro de una aplicación web.

### Ruta oculta
Página o sección existente dentro de una aplicación que no siempre es visible desde el menú principal.

### Control de acceso
Mecanismo que determina qué usuarios pueden o no acceder a ciertas funciones o secciones del sistema.

### Broken Access Control
Vulnerabilidad donde un usuario puede acceder o ejecutar acciones que no debería poder realizar.

---

## Actividad práctica realizada

Durante este laboratorio se realizó una prueba de descubrimiento de rutas ocultas dentro del sitio:

```bash
dirb http://fakebank.thm
