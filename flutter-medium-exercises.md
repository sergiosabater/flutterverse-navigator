# Ejercicios Nivel Intermedio de Flutter

## Ejercicio 1: Gestor de Tareas con Estado

**Objetivo:** Crear una aplicación de lista de tareas con gestión de estado usando Provider o Riverpod.

**Requisitos:**
- Agregar, editar y eliminar tareas
- Marcar tareas como completadas
- Filtrar tareas por estado (todas, activas, completadas)
- Persistir datos usando SharedPreferences
- Implementar un contador de tareas pendientes

**Conceptos clave:** State management, Provider/Riverpod, SharedPreferences, StatefulWidget

---

## Ejercicio 2: Aplicación del Clima con API

**Objetivo:** Desarrollar una app que consulte una API meteorológica y muestre el clima actual.

**Requisitos:**
- Integrar API (OpenWeatherMap o similar)
- Mostrar temperatura, condiciones y pronóstico
- Implementar búsqueda de ciudades
- Añadir manejo de errores y estados de carga
- Caché de datos con tiempo de expiración
- UI responsiva con diferentes layouts

**Conceptos clave:** HTTP requests, Future, async/await, JSON parsing, Error handling

---

## Ejercicio 3: Carrusel de Imágenes con Animaciones

**Objetivo:** Crear un carrusel de imágenes con transiciones animadas personalizadas.

**Requisitos:**
- Deslizamiento horizontal con PageView
- Animaciones de entrada/salida personalizadas
- Indicadores de página
- Zoom y pan en las imágenes
- Lazy loading de imágenes
- Implementar Hero animations entre pantallas

**Conceptos clave:** AnimationController, Tween, PageController, GestureDetector, Hero

---

## Ejercicio 4: Formulario de Registro Complejo

**Objetivo:** Desarrollar un formulario multi-paso con validación avanzada.

**Requisitos:**
- 3-4 pasos de formulario
- Validación en tiempo real
- Campos: email, password, teléfono, fecha de nacimiento
- Confirmación de password
- Selección de país con dropdown
- Mostrar progreso del formulario
- Guardar datos temporalmente al cambiar de paso

**Conceptos clave:** Form, TextFormField, Validation, RegExp, Stepper

---

## Ejercicio 5: Chat con Base de Datos Local

**Objetivo:** Crear una aplicación de chat con almacenamiento local usando SQLite.

**Requisitos:**
- Lista de conversaciones
- Vista de mensajes individual
- Enviar y recibir mensajes (simulado)
- Timestamps y estado de lectura
- Búsqueda de mensajes
- Eliminar conversaciones
- Implementar paginación en la lista de mensajes

**Conceptos clave:** sqflite, FutureBuilder, ListView.builder, Database CRUD operations

---

## Ejercicio 6: App de Notas con Búsqueda y Categorías

**Objetivo:** Desarrollar una aplicación de notas con funcionalidades avanzadas.

**Requisitos:**
- Crear, editar, eliminar notas
- Categorías con colores personalizados
- Búsqueda en tiempo real
- Ordenar por fecha, título o categoría
- Vista de cuadrícula y lista
- Compartir notas como texto
- Tema claro/oscuro

**Conceptos clave:** SearchDelegate, GridView, Theme, Share plugin

---

## Ejercicio 7: Reproductor de Música

**Objetivo:** Crear un reproductor de música con controles completos.

**Requisitos:**
- Lista de canciones (de assets o archivos locales)
- Play, pause, next, previous
- Barra de progreso interactiva
- Shuffle y repeat
- Artwork de la canción
- Controles en pantalla de bloqueo
- Lista de reproducción

**Conceptos clave:** audioplayers, StreamBuilder, ValueNotifier, Duration

---

## Ejercicio 8: Galería de Fotos con Infinite Scroll

**Objetivo:** Implementar una galería que cargue imágenes dinámicamente desde una API.

**Requisitos:**
- Integrar API de imágenes (Unsplash, Pixabay)
- Infinite scroll con detección de final de lista
- Grid layout responsivo
- Pantalla de detalle con zoom
- Descargar imágenes a galería
- Favoritos guardados localmente
- Pull-to-refresh

**Conceptos clave:** ScrollController, Pagination, NetworkImage, Image caching

---

## Ejercicio 9: Calculadora de Propinas con Divisor de Cuenta

**Objetivo:** Crear una calculadora con animaciones y UI pulida.

**Requisitos:**
- Calcular propina por porcentaje
- Dividir cuenta entre personas
- Redondear hacia arriba/abajo
- Historial de cálculos
- Animaciones al cambiar valores
- Selector de moneda
- Modo horizontal y vertical

**Conceptos clave:** NumberFormat, OrientationBuilder, AnimatedContainer, Custom painters

---

## Ejercicio 10: App de Recetas con Navegación Compleja

**Objetivo:** Desarrollar una app de recetas con navegación anidada y tabs.

**Requisitos:**
- Bottom navigation con 3 tabs
- Lista de recetas por categoría
- Detalle de receta con ingredientes y pasos
- Navegación hacia recetas relacionadas
- Favoritos con persistencia
- Temporizador de cocina integrado
- Búsqueda y filtros

**Conceptos clave:** Navigation, Named routes, BottomNavigationBar, TabBarView, Timer

---

## Ejercicio Bonus: Dashboard con Gráficas

**Objetivo:** Crear un dashboard con diferentes tipos de gráficas interactivas.

**Requisitos:**
- Gráfico de líneas para tendencias
- Gráfico de barras para comparaciones
- Gráfico circular para porcentajes
- Filtros por rango de fechas
- Animaciones al cargar datos
- Exportar gráficas como imagen

**Conceptos clave:** fl_chart package, CustomPaint, DatePicker, Screenshot

---

## Consejos para los Ejercicios

1. **Arquitectura limpia:** Separa la lógica de negocio de la UI
2. **Manejo de errores:** Siempre implementa try-catch y estados de error
3. **Loading states:** Muestra indicadores mientras cargan los datos
4. **Responsive design:** Prueba en diferentes tamaños de pantalla
5. **Accesibilidad:** Añade Semantics widgets y textos descriptivos
6. **Testing:** Escribe tests unitarios para la lógica de negocio
7. **Performance:** Usa const constructors y evita rebuilds innecesarios

## Recursos Adicionales

- [Flutter Documentation](https://docs.flutter.dev/)
- [Pub.dev](https://pub.dev/) - Paquetes de la comunidad
- [Flutter Cookbook](https://docs.flutter.dev/cookbook)
- [DartPad](https://dartpad.dev/) - Practica en el navegador
