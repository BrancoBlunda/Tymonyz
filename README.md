# Tymonyz - Generador Automático de Videos de Noticias para TikTok

Este proyecto automatiza la creación y subida de videos de noticias a TikTok, utilizando IA para generar narraciones y procesamiento de video para crear contenido atractivo. Estuvo en producción subiendo las 5 noticias más importantes del día en Argentina. Cuenta: https://www.tiktok.com/@argnewsia

> **Nota importante**: Este proyecto utiliza el módulo [TikTok-Auto-Uploader](https://github.com/makiisthenes/TiktokAutoUploader) para la funcionalidad de subida de videos a TikTok. Este módulo es una dependencia externa y mantiene su propia licencia y términos de uso.

## 🚀 Características

- Obtención automática de noticias de diferentes fuentes
- Generación de narraciones usando IA
- Creación de videos con texto y audio
- Subida automática a TikTok
- Personalización de estilos y formatos de video

## 📋 Prerrequisitos

- Python 3.8 o superior
- Chrome/Chromium instalado
- Cuenta de TikTok
- Credenciales de las siguientes APIs:
  - Google Cloud (para TTS)
  - Gemini
  - MediaStack
  - DeepSeek
  - NewsData

## 🛠️ Instalación

1. Clona el repositorio:
```bash
git clone https://github.com/BrancoBlunda/Tymonyz.git
cd tymonyz
```

2. Instala las dependencias:
```bash
pip install -r requirements.txt
```

3. Configura las variables de entorno:
```bash
cp .env.example .env
```
Edita el archivo `.env` con tus credenciales y configuraciones.

## 📁 Estructura del Proyecto

```
tymonyz/
├── assets/
│   ├── audios/         # Archivos de audio generados
│   ├── background_videos/  # Videos de fondo
│   ├── fonts/          # Fuentes para el texto
│   └── texts/          # Archivos de texto
├── credentials/        # Credenciales y configuraciones
├── src/               # Código fuente
│   ├── TiktokAutoUploader/  # Módulo de subida a TikTok
│   └── ...            # Otros módulos
└── extra/             # Archivos adicionales
```

## 🔧 Configuración

1. **APIs y Credenciales**:
   - Obtén las credenciales necesarias de cada servicio
   - Configúralas en el archivo `.env`

2. **Cuenta de TikTok**:
   - Ejecuta el script de login para configurar tu cuenta:
   ```bash
   python src/TiktokAutoUploader/cli.py login --name tu_usuario
   ```

## 🎯 Uso

Para ejecutar el generador de videos:

```bash
python src/main.py
```

El script:
1. Obtendrá las noticias más recientes
2. Generará narraciones usando IA
3. Creará videos con texto y audio
4. Subirá los videos a TikTok

## ⚙️ Configuración Personalizada

Puedes personalizar varios aspectos del proyecto editando el archivo `.env`:

- Rutas de archivos
- Tamaño y estilo de fuente
- Volumen de audio
- Y más...

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor, abre un issue primero para discutir los cambios que te gustaría hacer.

## 📝 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

## 👥 Autor

- **Branco Blunda** · [GitHub](https://github.com/BrancoBlunda) · [Portafolio](https://brancoblunda.github.io)

## 🙏 Agradecimientos

- [TikTok-Auto-Uploader](https://github.com/ultrafunkamsterdam/undetected-chromedriver) - Módulo principal para la subida de videos a TikTok
- [MoviePy](https://zulko.github.io/moviepy/) - Para el procesamiento de video
- [Google Cloud TTS](https://cloud.google.com/text-to-speech) - Para la generación de voz
- [Gemini API](https://ai.google.dev/) - Para la generación de contenido
- [MediaStack](https://mediastack.com/) - Para la obtención de noticias
- [DeepSeek](https://deepseek.ai/) - Para el procesamiento de IA
- [NewsData](https://newsdata.io/) - Para fuentes adicionales de noticias 
