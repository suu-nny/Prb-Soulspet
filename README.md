# Prb-Soulspet
# 🐾 SoulsPets

> Centro de cuidado profesional para perros y gatos.  
> Plataforma web de reservas construida con PHP, MySQL, HTML, CSS y JavaScript puro.

---

## 🗺️ Roadmap del Proyecto

```
Semana  1 ──────── 2 ──────── 3 ──────── 4 ──────── 5 ──────── 6 ✓
         │◄────── Sprint 1 ──────►│◄────── Sprint 2 ──────►│◄─── Sprint 3 ───►│
         │  Frontend & Diseño     │  Backend PHP            │  BD & Despliegue  │
```

---

### 🟣 Sprint 1 — Frontend & Diseño Visual `Semanas 1–2` `47 pts`

> **Objetivo:** Construir toda la interfaz visual: páginas, estilos, componentes y responsive design. El sitio se puede navegar visualmente sin lógica de servidor.

| # | Tarea | Estado |
|---|-------|--------|
| PB-01 | Sistema de estilos CSS (variables, tipografía, reset) | ✅ Done |
| PB-02 | Header con logo y menú hamburguesa responsive | ✅ Done |
| PB-03 | Footer con contacto y navegación | ✅ Done |
| PB-04 | Homepage: hero con galería, trust bar, features, CTA | ✅ Done |
| PB-05 | Página de servicios: cards con precios y horarios | ✅ Done |
| PB-06 | Páginas login y registro: formularios con validación JS | ✅ Done |
| PB-07 | Página reservar: layout con formulario y mascotas | ✅ Done |
| PB-08 | Mis reservas: tabla con badges de estado por color | ✅ Done |
| PB-09 | Perfil: formularios editar nombre / cambiar contraseña | ✅ Done |
| PB-10 | Panel admin: barra de navegación + banner de bienvenida | ✅ Done |
| PB-11 | JavaScript: hamburguesa, flash messages, confirmaciones | ✅ Done |

---

### 🟢 Sprint 2 — Backend PHP `Semanas 3–4` `44 pts`

> **Objetivo:** Implementar toda la lógica del servidor: autenticación, sesiones, CRUD de mascotas y reservas, panel admin funcional y seguridad.  
> ⚠️ En este sprint **no se toca la base de datos (SQL/esquema)** ni configuraciones de hosting.

| # | Tarea | Estado |
|---|-------|--------|
| PB-12 | `config/database.php`: conexión PDO con manejo de errores | ✅ Done |
| PB-13 | Registro: validación, hash bcrypt, auto-login | ✅ Done |
| PB-14 | Login / Logout: sesiones, roles, redirección por rol | ✅ Done |
| PB-15 | Mascotas: agregar y listar por usuario logueado | ✅ Done |
| PB-16 | Reservas: validación de disponibilidad, inserción, cancelación | ✅ Done |
| PB-17 | Perfil: actualizar nombre + cambiar contraseña con verificación | ✅ Done |
| PB-18 | Admin dashboard: contadores en tiempo real | ✅ Done |
| PB-19 | Admin reservas: listado, filtros y cambio de estado | ✅ Done |
| PB-20 | Admin usuarios: lista con estadísticas (JOIN) | ✅ Done |
| PB-21 | Protección de rutas: sesión + rol en cada página | ✅ Done |

---

### 🟠 Sprint 3 — Base de Datos & Despliegue `Semanas 5–6` `40 pts`

> **Objetivo:** Diseñar el esquema SQL final, configurar el entorno de producción en hosting, subir el proyecto, activar SSL y entregar el sistema validado.

| # | Tarea | Estado |
|---|-------|--------|
| PB-22 | Esquema SQL completo: tablas, FK, datos iniciales | ✅ Done |
| PB-23 | `setup.php`: script de configuración para producción | ✅ Done |
| PB-24 | Selección de plan de hosting (cPanel) y dominio | ✅ Done |
| PB-25 | Crear BD MySQL en hosting y ajustar `config/database.php` | ✅ Done |
| PB-26 | Importar `soulspet.sql` y verificar integridad en producción | ✅ Done |
| PB-27 | Subida de archivos al hosting por FTP / File Manager | ✅ Done |
| PB-28 | Pruebas funcionales completas en producción | ✅ Done |
| PB-29 | Configuración de HTTPS / SSL (Let's Encrypt) | ✅ Done |
| PB-30 | Documentación final y entrega al cliente | ✅ Done |

---

## 👥 Equipo — Metodología SCRUM

| Rol | Miembro | Responsabilidad |
|-----|---------|-----------------|
| 🎯 Product Owner | **Jamil** | Define la visión del producto, prioriza el backlog y aprueba entregables |
| 🔄 Scrum Master | **Bony** | Facilita el proceso SCRUM, organiza ceremonias y elimina impedimentos |
| 💻 Developer | **Johann** | Implementa todas las funcionalidades del sistema |

---

## ⚙️ Tech Stack

| Tecnología | Uso |
|-----------|-----|
| PHP | Lógica del servidor (backend) |
| MySQL + PDO | Base de datos con prepared statements |
| HTML / CSS | Estructura y estilos (sin frameworks) |
| JavaScript | Interactividad del cliente |
| XAMPP | Entorno de desarrollo local |
| cPanel Hosting | Entorno de producción |

---

## 🔐 Seguridad

- `password_hash()` + `password_verify()` — contraseñas cifradas con bcrypt
- PDO Prepared Statements — protección contra SQL Injection
- `htmlspecialchars()` — protección contra XSS
- Sesiones PHP con verificación de rol en cada ruta protegida

---

## 📁 Estructura del proyecto

```
soulspet/
├── admin/                  → Panel de administración
│   ├── index.php           → Dashboard con estadísticas
│   ├── reservas.php        → Gestión de reservas
│   ├── usuarios.php        → Lista de clientes
│   └── login.php           → Login exclusivo admin
├── assets/
│   ├── css/style.css       → Estilos (dark mode, responsive)
│   └── js/script.js        → JavaScript puro
├── config/
│   └── database.php        → Conexión PDO a MySQL
├── database/
│   └── soulspet.sql        → Script SQL completo
├── includes/
│   ├── header.php          → Header compartido
│   └── footer.php          → Footer compartido
├── index.php               → Página principal
├── login.php               → Login de clientes
├── registro.php            → Registro de clientes
├── reservar.php            → Hacer una reserva
├── mis_reservas.php        → Historial de citas
├── perfil.php              → Editar perfil
└── servicios.php           → Catálogo de servicios
```

---

## 🚀 Instalación rápida (XAMPP)

```bash
# 1. Copiar carpeta
C:\xampp\htdocs\soulspet\

# 2. Importar base de datos
# Abrir phpMyAdmin → Nueva BD "soulspet" → Importar database/soulspet.sql

# 3. Configurar (una sola vez)
http://localhost/soulspet/setup.php

# 4. Acceder
http://localhost/soulspet/
```

**Admin por defecto:** `admin@soulspet.com` / `Admin123`

---

*SoulsPets © 2025 — Porque cada alma merece el mejor cuidado 🐾*
