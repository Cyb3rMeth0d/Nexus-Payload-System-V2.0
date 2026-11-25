<div align="center">

<!-- Reemplaza esta ruta con tu propio banner o logo en la carpeta assets/ -->
<img src="assets/banner.png" alt="NexusPayload V2.0 Banner" width="100%" />

# ⚡ NexusPayload V2.0

**Gestor integral de payloads, repositorios remotos y administrador avanzado de procesos en tiempo real para PlayStation 5.**

Inspirado en la arquitectura de *PS5 Payload Manager*, diseñado para ofrecer velocidad, control total del sistema y una interfaz moderna sin fricciones.

<p align="center">
  <img src="https://img.shields.io/badge/Versión-2.0.0-0070D1?style=for-the-badge&logo=playstation&logoColor=white" alt="Versión 2.0.0" />
  <img src="https://img.shields.io/badge/Plataforma-PS5-00439C?style=for-the-badge&logo=playstation5&logoColor=white" alt="Plataforma PS5" />
  <img src="https://img.shields.io/badge/Estado-Estable-2EA44F?style=for-the-badge" alt="Estado Estable" />
  <img src="https://img.shields.io/badge/Licencia-MIT-F59E0B?style=for-the-badge" alt="Licencia MIT" />
</p>

<p align="center">
  <a href="#-descripción-general">Descripción</a> •
  <a href="#-características-principales">Características</a> •
  <a href="#-novedades-v20">Novedades V2.0</a> •
  <a href="#-capturas-de-pantalla">Capturas</a> •
  <a href="#-instalación">Instalación</a> •
  <a href="#-guía-de-uso">Uso</a> •
  <a href="#-roadmap">Roadmap</a>
</p>

</div>

---

## 📖 Descripción General

**NexusPayload V2.0** es una utilidad ligera y de alto rendimiento creada para centralizar la administración del entorno *homebrew* en PlayStation 5. Basado en el concepto de **PS5 Payload Manager**, esta segunda versión rediseña por completo el motor de comunicación, añade integración directa con **repositorios remotos de payloads** y mejora el control de ejecución en memoria.

Con **NexusPayload V2.0** puedes explorar catálogos online siempre actualizados, enviar archivos `.bin` o `.elf` a tu consola con un clic y supervisar los **procesos abiertos**, permitiéndote cargar, descargar, reiniciar o liberar módulos activos en tiempo real sin necesidad de reiniciar la consola.

---

## ✨ Características Principales

* 🌐 **Carga desde Repositorios Remotos (Payload Store):** Conecta repositorios online (GitHub o listas JSON personalizadas) para explorar, descargar e inyectar las últimas versiones de tus payloads sin transferir archivos manualmente.
* 🚀 **Inyección Instantánea Local y Remota:** Soporte nativo para archivos `.bin` y `.elf` mediante envío directo por red (TCP/Socket) o caché local, con verificación previa de integridad.
* 🔄 **Descarga y Liberación Dinámica:** Detén y descarga payloads o demonios (*daemons*) en ejecución de forma segura, liberando recursos del sistema al instante.
* 📊 **Administrador de Procesos Abiertos:** Monitorización en vivo de todos los procesos activos en el sistema (nombre, PID, estado de ejecución y uso de memoria) con opciones de filtrado rápido.
* 🔌 **Conexión Inteligente con PS5:** Detección automática de estado de red, reconexión persistente, prueba de latencia (*ping*) y soporte para múltiples perfiles de consola.
* 📂 **Biblioteca Organizada y Favoritos:** Clasifica tus payloads locales y remotos por categorías (Utilidades, Depuración, Juegos, Red), fija favoritos y ejecuta secuencias de carga automática (*Auto-Load*).
* 🛡️ **Protección Anti-Colisiones:** Sistema de prevención que detecta si un payload o servicio ya se encuentra inyectado en memoria para evitar bloqueos o *kernel panics*.
* 📝 **Consola de Registros (Logs) en Tiempo Real:** Visualiza la respuesta exacta de la consola, descargas desde repositorios, puertos activos y trazas de depuración.

---

## 🆕 Novedades V2.0 (Comparativa)

La versión **2.0** representa una reescritura enfocada en la conectividad remota, el control de procesos y la estabilidad frente a la primera generación:

| Característica | NexusPayload V1.0 | NexusPayload V2.0 |
| :--- | :---: | :---: |
| **Carga desde Repositorios Online** | ❌ Solo archivos locales | ✅ Catálogo remoto + descarga directa |
| **Envío de Payloads (`.bin` / `.elf`)** | ✅ Básico | ✅ Optimizado con verificación CRC |
| **Descarga / Cierre de Payloads** | ❌ No disponible | ✅ Completo en tiempo real |
| **Administrador de Procesos Abiertos** | ⚠️ Solo lectura básica | ✅ Control total (Filtrado, PID, Cierre) |
| **Detección de Doble Inyección** | ❌ Manual | ✅ Automática con alerta preventiva |
| **Perfiles y Carga por Lotes** | ❌ No soportado | ✅ Múltiples perfiles y *Auto-Load* |
| **Consola de Logs Integrada** | ⚠️ Limitada | ✅ Tiempo real con exportación |
| **Velocidad de Respuesta y UI** | Estándar | ⚡ Hasta 3x más rápida y rediseñada |

---

## 📋 Requisitos Previos

Antes de utilizar **NexusPayload V2.0**, asegúrate de contar con lo siguiente:

1. **Consola PlayStation 5** con firmware compatible y acceso a ejecución de *homebrew* (WebKit, BD-JB, Lua, etc.).
2. **Receptor de Payloads activo** en la PS5 (por ejemplo, *elfldr*, *etaHEN* o cargador equivalente escuchando en los puertos `9020` / `9021`).
3. **Misma red local (LAN / Wi-Fi)** entre la consola y el dispositivo desde donde ejecutas NexusPayload (se recomienda conexión por cable Ethernet para mayor estabilidad).
4. **Acceso a Internet** (opcional, únicamente necesario para sincronizar y descargar payloads desde repositorios remotos).

---

## ⚙️ Instalación

### Opción 1: Descarga directa (Recomendada)
1. Dirígete a la sección de [**Releases**](https://github.com/TU_USUARIO/NexusPayload-V2/releases) del repositorio.
2. Descarga la última compilación de **NexusPayload V2.0** para tu sistema.
3. Descomprime el archivo en una carpeta de tu elección y ejecuta el binario principal.

### Opción 2: Clonar el repositorio
```bash
# Clonar el repositorio oficial
git clone [https://github.com/TU_USUARIO/NexusPayload-V2.git](https://github.com/TU_USUARIO/NexusPayload-V2.git)

# Acceder al directorio del proyecto
cd NexusPayload-V2
```

<details>
<summary><b>🔧 Configuración avanzada (config.json)</b></summary>

Puedes personalizar los parámetros predeterminados y añadir tus propias fuentes de repositorios editando el archivo `config.json` en la raíz del proyecto:

```json
{
  "console_ip": "192.168.1.100",
  "default_port": 9021,
  "process_manager_port": 9030,
  "timeout_ms": 5000,
  "auto_refresh_processes": true,
  "refresh_interval_ms": 2000,
  "prevent_duplicate_injection": true,
  "cache_remote_payloads": true,
  "payload_repositories": [
    "[https://raw.githubusercontent.com/TU_USUARIO/ps5-payloads-repo/main/manifest.json](https://raw.githubusercontent.com/TU_USUARIO/ps5-payloads-repo/main/manifest.json)"
  ]
}
```
</details>

---

## 🚀 Guía de Uso

### 1. Vincular tu PlayStation 5
1. Enciende tu PS5 y activa tu *exploit* / cargador de payloads habitual.
2. Abre **NexusPayload V2.0** e introduce la **dirección IP local** de tu consola (puedes verla en *Ajustes > Red > Estado de conexión*).
3. Verifica que el indicador de estado cambie a **Conectado** (verde).

### 2. Cargar un Payload (Local o desde Repositorio)
* **Desde Repositorios Online:**
  1. Abre la pestaña **Repositorios** y pulsa **Actualizar índice** para obtener las últimas versiones disponibles.
  2. Selecciona el payload deseado y elige **Inyectar directamente** (envío al vuelo a la consola) o **Descargar a biblioteca** (para uso sin conexión).
* **Desde Archivo Local:**
  1. Selecciona un payload guardado en tu **Biblioteca** o haz clic en **Importar archivo** (`.bin` / `.elf`).
  2. Pulsa en **Cargar Payload** y confirma la inyección en la consola de logs.

### 3. Administrar Procesos y Descargar Payloads
1. Abre la pestaña **Procesos Abiertos**.
2. Utiliza la barra de búsqueda para localizar el módulo o servicio activo por nombre o **PID**.
3. Selecciona el proceso deseado y elige una acción:
   * **Descargar / Detener:** Finaliza el payload de forma limpia y libera su memoria.
   * **Reiniciar:** Descarga y vuelve a inyectar el módulo en un solo paso.
   * **Inspeccionar:** Muestra detalles de hilos, puertos asociados y tiempo de actividad.

---

## 🗂️ Estructura del Proyecto

```text
NexusPayload-V2/
├── assets/                 # Recursos visuales, iconos y capturas del README
├── payloads/               # Directorio local y caché de payloads descargados (.bin / .elf)
├── src/
│   ├── core/               # Motor de sockets, envío de payloads y control de red
│   ├── repo/               # Gestor de repositorios remotos, índices JSON y caché
│   ├── process/            # Módulo de lectura, filtrado y descarga de procesos PS5
│   ├── ui/                 # Componentes de interfaz gráfica y temas
│   └── utils/              # Validación CRC, logs y gestión de configuración
├── config.json             # Archivo de configuración de red, puertos y repositorios
├── LICENSE                 # Licencia MIT
└── README.md               # Documentación principal
```

---

## 🗺️ Roadmap

- [x] Motor de inyección rápida para `.bin` y `.elf`
- [x] Soporte para carga remota y descarga desde repositorios online (Payload Store)
- [x] Administrador de procesos abiertos en tiempo real
- [x] Función de descarga y liberación segura de payloads
- [x] Sistema de logs detallados y detección de duplicados
- [ ] Monitor de temperaturas (SoC / CPU) y telemetría de hardware en vivo
- [ ] Gestión integrada de plugins para *etaHEN*
- [ ] Interfaz web remota para controlar la consola desde el navegador móvil

---

## 🤝 Contribuciones

Las contribuciones son bienvenidas y ayudan a mejorar la herramienta para toda la comunidad:

1. Haz un **Fork** del proyecto.
2. Crea una nueva rama para tu mejora (`git checkout -b feature/nueva-funcion`).
3. Realiza tus cambios y haz commit (`git commit -m 'Añade nueva función'`).
4. Sube los cambios a tu rama (`git push origin feature/nueva-funcion`).
5. Abre un **Pull Request**.

---

## 🙏 Créditos y Agradecimientos

* Inspirado en el trabajo original de **PS5 Payload Manager** y las herramientas de gestión de la escena PS5.
* Agradecimientos especiales a todos los desarrolladores de *payload loaders* y *homebrew* de PlayStation 5 por mantener activo el ecosistema.

---

## ⚠️ Aviso Legal

Este software ha sido desarrollado únicamente con fines educativos, de investigación y para la gestión legítima de software *homebrew* en consolas de tu propiedad. El autor no se hace responsable del mal uso de esta herramienta ni de posibles daños derivados de la ejecución de código no verificado.

---

<div align="center">

Desarrollado con 💙 para la comunidad de PlayStation 5

**NexusPayload V2.0** — *Control total sobre tus repositorios, payloads y procesos.*

</div>
