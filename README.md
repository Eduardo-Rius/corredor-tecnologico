# Código de Expansión 90

Este es el proyecto oficial del embudo interactivo "Código de Expansión 90", una aplicación web de 6 fases construida en Vanilla HTML, CSS y JS, diseñada con temática oscura, inmersiva, futurista y con estética superior (Glassmorphism + Neo-morphism).

## 🚀 Arquitectura del Embudo

El proyecto funciona como una pasarela estricta en donde la secuencia y el compromiso del usuario actúan como filtro. Consta de 6 archivos:

1. **`pagina-1.html` (Landing de Introducción)**: Presenta la promesa del proyecto y guarda el inicio del trayecto en caché.
2. **`pagina-2.html` (Ruta de Videos Clave)**: Sistema secuencial de 3 videos usando la API de IFrame de YouTube, validando que uno finalice para desbloquear el siguiente.
3. **`pagina-3.html` (Evaluación de Asimilación)**: Sistema dinámico con un banco interno de preguntas aleatorizadas (30 reactivos). El usuario debe alcanzar mínimo un 8/10 para avanzar a la Fase 4.
4. **`pagina-4.html` (El Motor del Toroide)**: Una intro audiovisual poderosa bloqueando el contenido si no se asimilaron las bases primero.
5. **`pagina-5.html` (Compromiso Final)**: Diseño premium enalteciendo la escasez y dando entrada a la fase de pre-pago/inscripción.
6. **`pagina-6.html` (CRM y Base de Datos)**: Formulario estilizado para captación de datos (Nombre, ciudad, celular, e-mail...) que extrae invisiblemente la nota y calificación de la base de datos local y viaja transparentemente a Google Sheets empleando Google Apps Scripts a través de URL-Encoding.

## 🔐 Seguridad y Funcionalidades
Todo el sistema está enlazado a nivel de variables de estado local (`localStorage`). Todas las páginas validan (en el código DOMContentLoaded) si el usuario superó los retenes requeridos en el pasado; si intenta hacer trampa, escudos de redireccionamiento lo rebotan al sitio de abandono previo. No requiere base de datos pesada intermedia (SQL/NoSQL) ya que la terminal final funge de CRM usando un Google Sheet de recepción directa.

---
**Build instructions**:  
No se requieren empaquetadores (webpack) ni frameworks reactivos. Sirve de forma nativa abriéndose en cualquier entorno de host, Vercel, Netlify o Cloudflare Pages al hacer tracking directo con el branch `main`.
