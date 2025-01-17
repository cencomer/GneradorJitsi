# Generador de Enlaces para Reuniones Jitsi

Una aplicación web simple y elegante para generar enlaces personalizados de reuniones Jitsi Meet.

## 🚀 Características

- Generación de enlaces únicos para reuniones
- Personalización de parámetros de la reunión:
  - Protección con contraseña
  - Silenciar al entrar
  - Límite de participantes
- Historial de reuniones recientes
- Interfaz responsive y amigable
- Generación de enlaces de administración
- Función de copiado rápido del mensaje de invitación

## 🛠️ Tecnologías Utilizadas

- HTML5
- JavaScript (ES6+)
- Tailwind CSS
- LocalStorage para persistencia de datos

## 📋 Requisitos Previos

- Navegador web moderno
- Conexión a Internet (para cargar Tailwind CSS CDN)

## 🔧 Instalación

1. Clona el repositorio:
```bash
git clone [URL_DEL_REPOSITORIO]
```

2. Abre el archivo `index.html` en tu navegador web preferido

## 💻 Uso

1. Completa los campos requeridos:
   - Nombre del organizador
   - Usuario para la reunión
   - Empresa (opcional)

2. Configura las opciones de la reunión:
   - Activar/desactivar protección con contraseña
   - Activar/desactivar silencio al entrar
   - Establecer número máximo de participantes

3. Haz clic en "Generar Enlace"

4. Utiliza las opciones disponibles:
   - Copiar mensaje de invitación
   - Acceder al enlace de la reunión
   - Acceder al panel de administración

## 🔍 Funcionalidades Principales

### Generación de Enlaces
```javascript
async function generateMeeting() {
    // Genera un UUID único para cada reunión
    const uuid = crypto.randomUUID();
    const meetingName = `${user}-${uuid}`;
    const meetingLink = `https://meet.jit.si/${meetingName}`;
}
```

### Gestión de Reuniones Recientes
```javascript
function saveRecentMeeting(meetingData) {
    const recentMeetings = JSON.parse(localStorage.getItem('recentMeetings') || '[]');
    recentMeetings.unshift(meetingData);
    localStorage.setItem('recentMeetings', JSON.stringify(recentMeetings.slice(0, 5)));
}
```

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Para cambios importantes:

1. Haz un Fork del repositorio
2. Crea una nueva rama
3. Realiza tus cambios
4. Envía un Pull Request

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE.md](LICENSE.md) para más detalles.

## ✨ Agradecimientos

- [Tailwind CSS](https://tailwindcss.com/)
- [Jitsi Meet](https://meet.jit.si/)