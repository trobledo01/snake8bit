# 🐍 snake8bit

Un juego clásico de Snake con estética **8-bit/retro**, desarrollado con **Flutter Web**. Jugable directamente desde el navegador, sin necesidad de instalación.

---

## 🎮 Demo

> Abre `index.html` en un servidor local o despliega la carpeta en cualquier hosting estático.

---

## 🕹️ ¿Cómo jugar?

- **↑ ↓ ← →** — Mueve la serpiente
- Come la comida para crecer y acumular puntos
- Evita chocar contra las paredes o contra ti mismo
- ¡Intenta superar tu récord!

---

## 🚀 Tecnologías

| Tecnología | Descripción |
|------------|-------------|
| [Flutter](https://flutter.dev/) | Framework principal (Web) |
| Dart | Lenguaje de programación |
| CanvasKit / SkWasm | Motor de renderizado gráfico |
| PWA | Soporte como Progressive Web App |

---

## 📁 Estructura del proyecto

```
snake8bit/
├── index.html                  # Punto de entrada de la app
├── main.dart.js                # Código compilado de Flutter
├── flutter.js                  # Inicializador del motor Flutter
├── flutter_service_worker.js   # Service Worker para PWA
├── manifest.json               # Manifiesto de la Web App
├── favicon.png                 # Ícono del sitio
├── assets/                     # Fuentes y recursos
├── canvaskit/                  # Motor de renderizado (CanvasKit + SkWasm)
└── icons/                      # Íconos para PWA (192x192, 512x512)
```

---

## 🌐 Despliegue local

Necesitas servir los archivos desde un servidor HTTP (no abrir el `index.html` directo por limitaciones de CORS con Flutter Web).

### Opción 1 — Python

```bash
cd snake8bit/
python3 -m http.server 8080
```

Abre en el navegador: [http://localhost:8080](http://localhost:8080)

### Opción 2 — Node.js (`serve`)

```bash
npx serve snake8bit/
```

### Opción 3 — VS Code

Instala la extensión **Live Server** y abre `index.html` con ella.

---

## ☁️ Despliegue en producción

Este proyecto es un build estático de Flutter Web, compatible con cualquier hosting estático:

- **GitHub Pages** — Sube el contenido de la carpeta al branch `gh-pages`
- **Netlify / Vercel** — Arrastra y suelta la carpeta en el dashboard
- **Firebase Hosting** — Usa `firebase deploy` apuntando a esta carpeta como `public`

---

## 🛠️ Compilado desde Flutter

Este repositorio contiene el **build de producción** generado con:

```bash
flutter build web --release
```

Si deseas modificar el código fuente, necesitas el proyecto Dart original y Flutter instalado:

```bash
# Requisitos
flutter --version   # Flutter 3.x o superior recomendado
dart --version
```

---

## 📱 PWA

`snake8bit` funciona como **Progressive Web App**: puedes instalarlo en tu dispositivo desde el navegador (Chrome / Edge → "Instalar aplicación").

---

## 📄 Licencia

MIT — libre para usar, modificar y distribuir.
