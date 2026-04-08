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

La herramienta *DIRB* permitió identificar recursos internos expuestos en la aplicación web.

### Rutas encontradas
•⁠  ⁠⁠ /bank-transfer ⁠
•⁠  ⁠⁠ /images ⁠

---

## Interpretación del resultado

La ruta ⁠ /bank-transfer ⁠ respondió correctamente, lo que indicó que existía una funcionalidad activa dentro de la aplicación.

Al acceder manualmente a esta ruta desde el navegador, se observó un *panel administrativo* que permitía registrar depósitos en cuentas bancarias internas.

Esto demostró un caso de *funcionalidad sensible expuesta sin controles de acceso adecuados*.

---

## Validación del hallazgo

Dentro del panel encontrado se realizó una acción controlada en el laboratorio:

•⁠  ⁠Cuenta seleccionada: ⁠ 8881 ⁠
•⁠  ⁠Monto ingresado: ⁠ $2000 ⁠

Con esto se comprobó que la funcionalidad no solo existía, sino que además estaba operativa y podía ser utilizada sin restricciones visibles.

---

## Herramienta utilizada

### DIRB
Herramienta de enumeración web utilizada para descubrir directorios, rutas y recursos ocultos dentro de una aplicación.

---

## Lo más importante que aprendí

•⁠  ⁠Cómo funciona la *seguridad ofensiva* a nivel introductorio.
•⁠  ⁠Qué es la *enumeración web*.
•⁠  ⁠Cómo una ruta oculta puede exponer una función sensible.
•⁠  ⁠La diferencia entre *descubrir una ruta* y *validar una vulnerabilidad*.
•⁠  ⁠Cómo una mala implementación de permisos puede derivar en *acceso no autorizado*.

---

## Relación con el mundo real

Este tipo de error puede presentarse en aplicaciones reales cuando:

•⁠  ⁠existen paneles administrativos expuestos
•⁠  ⁠no se validan correctamente los permisos del usuario
•⁠  ⁠una función interna puede ser utilizada desde una URL directa

Esto representa un riesgo importante porque puede permitir acciones sensibles sin autorización.

---

## Evidencia

### Vista del módulo completado
La siguiente captura muestra la finalización exitosa del laboratorio en TryHackMe:

![Captura final del módulo](./captura-final-real.png) 
---

## Reflexión personal

Este módulo me ayudó a entender que la seguridad ofensiva no se trata de “hackear por hackear”, sino de aprender a identificar debilidades reales en sistemas y aplicaciones desde una perspectiva ética y profesional.

También comprendí la importancia de la enumeración web como una fase inicial clave para descubrir superficies de ataque y validar posibles vulnerabilidades.

Este ejercicio fortaleció mi comprensión de cómo un atacante puede encontrar funciones ocultas y por qué los controles de acceso son esenciales en la seguridad de aplicaciones web.
