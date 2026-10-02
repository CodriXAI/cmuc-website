# Colegio Mayor Universitario de Córdoba - Sitio Web

Sitio web oficial del Colegio Mayor Universitario de Córdoba (CMUC), una institución educativa sin fines de lucro fundada en la década del 50 por el monseñor Eladio Bordagaray.

🌐 **Sitio en vivo**: [https://colegiomayorcba.com.ar](https://colegiomayorcba.com.ar)

## 🏛️ Acerca del Proyecto

Este sitio web presenta la historia, valores y servicios del Colegio Mayor Universitario de Córdoba, que se rige bajo tres pilares fundamentales:
- **Estudio**
- **Colaboración** 
- **Integración**

## 🚀 Tecnologías Utilizadas

- **Backend**: PHP
- **Frontend**: HTML5, CSS3, JavaScript
- **Framework CSS**: Bootstrap 4
- **Iconos**: Font Awesome
- **Email**: SMTP con Gmail
- **Hosting**: Ferozoo
- **Dominio**: colegiomayorcba.com
- **Desarrollo**: Ngrok (túneles públicos)

## 📋 Características

- ✅ Diseño responsivo y moderno
- ✅ Galería de imágenes con modales
- ✅ Formulario de contacto funcional
- ✅ Información institucional completa
- ✅ Enlaces a documentos históricos (PDFs)
- ✅ Integración con redes sociales
- ✅ Mapa de ubicación
- ✅ Build automático para producción
- ✅ Deployment optimizado

## 🛠️ Instalación y Configuración

### Prerrequisitos

- PHP 7.2+
- Composer (gestor de dependencias de PHP)

### Instalación

1. Clona el repositorio:
```bash
git clone https://github.com/tu-usuario/cmuc-website.git
cd cmuc-website
```

2. Instala las dependencias:
```bash
composer install
```

3. Configura las variables de entorno:
   - Copia el archivo `.env.example` a `.env`
   - Completa las configuraciones necesarias

### Configuración del Email

Para que el formulario de contacto funcione, necesitas configurar:

1. **Gmail App Password**: 
   - Ve a tu cuenta de Google
   - Habilita la autenticación de 2 factores
   - Genera una contraseña de aplicación
   - Úsala en lugar de tu contraseña regular

2. **Configuración en el código**:
   - Edita `static/assets/mail/config.php`
   - Reemplaza `EMAIL_USER` y `EMAIL_PASSWORD` con tus credenciales

### Configuración de Ngrok (Opcional)

Para desarrollo con túnel público:
1. Regístrate en [ngrok.com](https://ngrok.com)
2. Obtén tu token de autenticación
3. Reemplaza el token en `server.py`

## 🚀 Ejecución

### Desarrollo Local

```bash
php -S localhost:8000
```

El sitio estará disponible en `http://localhost:8000`

### Producción

Para despliegue en producción, considera usar:
- **Apache** o **Nginx** como servidor web
- **SSL/TLS** para HTTPS

## 📁 Estructura del Proyecto

```
cmuc-website/
├── index.php              # Página principal
├── requirements.txt       # Dependencias de PHP
├── .gitignore            # Archivos ignorados por Git
├── static/               # Archivos estáticos
│   ├── css/             # Estilos CSS
│   ├── js/              # JavaScript
│   ├── img/             # Imágenes
│   └── assets/          # Documentos y recursos
│       └── mail/        # Backend de contacto (PHPMailer)
└── templates/           # Plantillas HTML
    └── index.html       # Página principal
```

## 📧 Configuración del Formulario de Contacto

El formulario incluye validación para:
- Nombre (requerido)
- Email (requerido, formato válido)
- Mensaje (requerido)

Los mensajes se envían automáticamente al email configurado.

## 🎨 Personalización

### Colores y Estilos
Edita `/static/css/styles.css` para modificar:
- Colores del tema
- Tipografías
- Espaciados
- Efectos visuales

### Imágenes
Reemplaza las imágenes en `/static/img/cmuc/` con:
- Formato recomendado: JPG/PNG
- Optimización para web
- Resolución apropiada para responsive design

### Contenido
Modifica `/templates/home.php` para actualizar:
- Textos institucionales
- Enlaces a documentos
- Información de contacto

## 🤝 Contribuir

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para detalles.

## 👥 Contacto

**Colegio Mayor Universitario de Córdoba**
- Email: colegiomayorcba@gmail.com
- Facebook: [@colegiomayorcba](https://www.facebook.com/colegiomayorcba/)
- Instagram: [@cmuc.cordoba](https://www.instagram.com/cmuc.cordoba/)
- Ubicación: Láprida 30/37, Nueva Córdoba, Córdoba

## 🙏 Reconocimientos

- Padre Eladio Bordagaray - Fundador del CMUC
- Departamento de Cultura - Desarrollo y mantenimiento
- Bootstrap Team - Framework CSS
- Font Awesome - Iconografía

---

*"No te conformes con ser bueno, ¡Sé santo!" - Padre Eladio Bordagaray*

# CMUC Website

Este sitio ahora funciona 100% con PHP y PHPMailer para el formulario de contacto. No requiere Python ni Flask.

## Ventajas de la migración a PHP
- **Compatibilidad total con hostings compartidos**: PHP es soportado por la mayoría de los proveedores (como Ferozo), sin configuraciones especiales.
- **Despliegue sencillo**: Solo subís los archivos, sin necesidad de entornos virtuales, dependencias ni servidores adicionales.
- **Menos mantenimiento**: No hay que preocuparse por versiones de Python, Flask o dependencias externas.
- **Seguridad y robustez**: PHPMailer es el estándar para envío de mails en PHP y permite usar SMTP autenticado.
- **Fácil de extender**: Si necesitás agregar lógica dinámica, PHP lo permite sin cambiar de stack.
- **Frontend igual de moderno**: Todo el diseño, animaciones y JS siguen funcionando igual que antes.

## Estructura principal
- index.php (página principal)
- static/ (CSS, JS, imágenes, PDFs)
- static/assets/mail/send_message.php (backend de contacto, usa PHPMailer)

## Migración
- Se eliminaron todos los archivos de backend Python y plantillas Flask.
- Para el formulario de contacto, configurar `static/assets/mail/config.php` según el ejemplo `config.sample.php`.

## Despliegue en Ferozo
Ver instrucciones detalladas en `README_FEROZO.md`.
