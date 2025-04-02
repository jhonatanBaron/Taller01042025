# 🏴‍☠️ ¡Ahoy! Bienvenido al Navío Traefik - Ejercicio #3 🏴‍☠️

¡Zarpemos en esta aventura, grumete! Esta infraestructura local está gobernada por el temido **Capitán Traefik**, quien controla el tráfico y protege la flota de servicios en este puerto virtual.

### ⚓ La Flota de Servicios

- 🦑 **Traefik**: El guardián del tráfico, nuestro proxy reverenciado, con su tablero de mando siempre vigilante.
- ⚓ **api-registro**: El escriba del barco, lleva el conteo de cuántas veces cada marinero (cliente) ha pasado por cubierta.
- 🐙 **cliente-app (x3)**: Tres intrépidos grumetes que reportan periódicamente al escriba.
- 🐠 **monitor**: El vigía, siempre atento a la actividad de la flota y las rutas activas.

---

## 🛠️ Herramientas del Pirata

Antes de zarpar, asegúrate de tener en tu cofre del tesoro:

- 🐋 **Docker**: Para desplegar los navíos.
- 📦 **Docker Compose**: Para coordinar la flota.

---

## 🏴‍☠️ ¡A Izar las Velas!

Primero, baja al puerto del proyecto:

```bash
cd ejercicio-3
```

Luego, ordena al capitán que levante anclas y despliegue la flota:

```bash
docker-compose up --build
```

💡 **Consejo de viejo lobo de mar:** Si no quieres que el capitán esté gritando en tu cara, añade `-d` para mantenerlo en silencio:

```bash
docker-compose up -d --build
```

---

## 🌊 Rutas para Navegar

Aquí están los puntos estratégicos donde podrás observar la acción:

| Servicio                  | Ruta                                           | ¿Qué verás?                                  |
|--------------------------|------------------------------------------------|----------------------------------------------|
| 🧭 **Tablero del Capitán** | [localhost:8080](http://localhost:8080)        | El mando del temido Traefik                   |
| 📜 **Registro de Bitácora**| [localhost/registro-status](http://localhost/registro-status) | Estado de las visitas de los grumetes |
| 🚤 **Grumete 1**           | [localhost/cliente/app1](http://localhost/cliente/app1) | La primera aplicación cliente                |
| 🚤 **Grumete 2**           | [localhost/cliente/app2](http://localhost/cliente/app2) | La segunda aplicación cliente                |
| 🚤 **Grumete 3**           | [localhost/cliente/app3](http://localhost/cliente/app3) | La tercera aplicación cliente                |
| 🔭 **El Vigía (Monitor)** | [localhost/monitor](http://localhost/monitor)  | El estado general del navío                   |

---

## 🗝️ Palabras Secretas del Capitán (Autenticación)

Para acceder a la bitácora del escriba (`/registro`), el capitán exige la contraseña secreta:

- **Usuario:** admin  
- **Contraseña:** password  

Si intentas acceder sin estos secretos, te quedarás afuera, como un simple marinero sin rango.

---

## ⚠️ Para Detener el Navío

Cuando el viento deje de soplar y sea momento de anclar, haz que el capitán detenga la flota:

```bash
docker-compose down
```

---

## 🗺️ Mapa del Tesoro - Estructura del Proyecto

```
ejercicio-3/
├── docker-compose.yml   # El grimorio que invoca la flota
├── traefik.yml          # Las órdenes del Capitán Traefik
├── api-registro/        # El escriba y su registro
├── cliente-app/         # Los grumetes que patrullan
└── monitor/             # El vigía que mantiene la guardia
```

---

## ⚓ Consejos de un Viejo Marinero

- La flota está unida bajo la bandera del capitán en la red `web`.
- El tablero del capitán solo se muestra cuando el viento sopla desde **localhost**. ¡No intentes acceder desde aguas lejanas!

---

¡Listo, grumete! Ahora navega por estas aguas digitales y mantén la flota bajo control. ¡Recuerda, el Capitán Traefik siempre vigila! 🏴‍☠️🌊
