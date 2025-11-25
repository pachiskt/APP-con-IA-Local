markdown
# Asistente Universitario IA

## Descripción
Asistente inteligente desarrollado en Flutter para la Universidad Continental que proporciona información académica, contactos oficiales y acceso a reglamentos mediante un sistema de IA local.

## Características Principales

### Chatbot Inteligente
- **200+ preguntas frecuentes** organizadas en 7 categorías
- **Sistema de IA local** con algoritmo BoW + TF-IDF mejorado
- **Respuestas inmediatas** sin necesidad de conexión a internet
- **Stemming en español** para mejor comprensión de consultas

### Gestión de Contactos
- **20 contactos oficiales** de la universidad
- **Acciones directas**: llamar, enviar WhatsApp, email
- **Horarios de atención** y departamentos específicos

### Biblioteca de Reglamentos
- **31 documentos PDF** organizados por categoría
- **Visualización integrada** con `open_file`
- **Búsqueda inteligente** por nombre y descripción

### Funcionalidades Técnicas
- **Arquitectura 100% offline** garantizando privacidad
- **Interfaz responsive** diseñada en Flutter
- **Tiempos de respuesta** < 500ms
- **Código modular** y fácil de mantener

Tecnologías Utilizadas

Frameworks y Librerías
- **Flutter 3.0+** - Framework principal
- **Dart** - Lenguaje de programación
- **url_launcher** - Integración con apps nativas
- **open_file** - Gestión de documentos PDF
- **path_provider** - Manejo de archivos locales

Algoritmos de IA
- **Bag-of-Words (BoW)** - Representación textual
- **TF-IDF** - Ponderación de términos importantes
- **Similitud Coseno** - Medición de relevancia
- **Stemming en español** - Normalización lingüística



Instalación y Configuración
Prerrequisitos
- Flutter SDK 3.0 o superior
- Dart 2.19 o superior
- Dispositivo Android/iOS o emulador

Pasos de Instalación
1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/tu-usuario/asistente-universitario.git
   cd asistente-universitario
Instalar dependencias
bash
flutter pub get
Ejecutar la aplicación
bash
flutter run
Configuración de PDFs
Los documentos deben ubicarse en:
text
assets/pdfs/
Y declararse en pubspec.yaml:
yaml
flutter:
  assets:
    - assets/pdfs/


Uso de la Aplicación


Chatbot Principal
Abre la pestaña "Chat"
Escribe tu pregunta en lenguaje natural
Recibe respuestas instantáneas con información verificada
Preguntas Frecuentes
Navega a "FAQs"
Usa la barra de búsqueda para encontrar temas específicos
Explora categorías organizadas
Contactos
Accede a "Contactos"
Filtra por departamento o tipo
Usa los botones de acción para contactar directamente
Reglamentos
Ve a "Reglamentos"
Busca documentos por nombre
Toca cualquier item para abrir el PDF
🔧 Personalización
Agregar Nuevas Preguntas
Edita chat_service.dart en la sección _baseConocimiento:
dart
'nueva_categoria': {
  'respuesta': 'Tu respuesta aquí...',
  'palabras_clave': _procesarTexto('lista de palabras clave relevantes')
}
Modificar Contactos
Actualiza la lista en contacts_screen.dart:
dart
{
  'departamento': 'Nuevo Departamento',
  'telefono': '+51 XXX XXX XXX',
  'email': 'email@continental.edu.pe',
  'tipo': 'Tipo de contacto',
  'horario': 'Horario de atención'
