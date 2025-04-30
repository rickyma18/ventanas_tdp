# Ventanas TDP

**Ventanas TDP** es una app Flutter responsiva para Wear OS 3+ diseñada para ayudar al árbitro asistente de la Tercera División Profesional (TDP) a gestionar los cambios de jugadores de forma rápida y confiable desde su smartwatch. Permite cargar datos clave de cada jugador, controlar los límites de 5 cambios con 3 ventanas y validar la conformación de las alineaciones según categoría (mayor, mediano, menor).

---

## 📋 Características

- **Multi-ventanas de cambio**: registra hasta 3 ventanas de sustituciones por partido.  
- **Límite de cambios**: contabiliza y bloquea a partir del quinto cambio.  
- **Validación de categorías**: garantiza que en los 11 titulares haya siempre 1 jugador menor y 2 medianos.  
- **Carga local**: almacena dorsal y categoría de cada jugador por equipo en memoria local para acceso instantáneo.  
- **UI responsiva para smartwatch**: layouts adaptados a circular y rectangular, botones grandes y navegación por gestos.  
- **Sincronización opcional**: exporta el registro de cambios a tu app móvil o servidor cuando te reconectas (opcional).

---

## 🚀 Requisitos

- Wear OS 3.0 o superior  
- Flutter 3.x con soporte Wear  
- SDK Android (API 31+)  
- Conexión Bluetooth para sincronización opcional  

---

## 🔧 Instalación y ejecución

1. **Clona el repositorio**  
   ```
   git clone https://github.com/rickyma18/VentanasTDP.git
   cd VentanasTDP
Instala dependencias




flutter pub get
Conecta tu reloj

Habilita modo desarrollador y ADB via Bluetooth.

Empareja tu Wear OS con el PC.

Verifica con:




adb devices
Ejecuta en Wear OS




flutter run -d <wear-device-id>
▶️ Uso
En la pantalla de Equipos, selecciona tu equipo local o visitante.

Pulsa “Cargar Jugadores” para importar desde JSON local o entrada manual.

En Alineación, revisa que haya 1 menor y 2 medianos en los titulares.

Navega a Ventana de Cambios (1–3).

Selecciona el dorsal a salir y el dorsal a entrar; la app validará automáticamente la categoría.

Confirma el cambio y repite hasta 5 cambios totales. La interfaz muestra cambios restantes y ventanas usadas.

Al finalizar, pulsa Exportar para enviar el registro a tu dispositivo móvil o servidor.

🗂️ Estructura de carpetas
text


lib/
├── model/
│   ├── player.dart         # Entidad jugador (dorsal, categoría)
│   └── substitution.dart   # Entidad cambio
├── services/
│   └── storage_service.dart# Gestión de memoria local
├── view/
│   ├── team_select_screen.dart
│   ├── lineup_screen.dart
│   └── substitution_screen.dart
├── viewmodel/
│   ├── team_vm.dart
│   ├── lineup_vm.dart
│   └── substitution_vm.dart
├── main.dart               # Punto de entrada Wear OS
└── theme.dart              # Temas y estilos responsivos

<div style="display:flex; flex-wrap:wrap; gap:10px; justify-content:center;">
  <img src="https://github.com/user-attachments/assets/82fcdcbe-4d4e-46f8-85a7-4cb3384b0f87" alt="Pantalla 1" width="200" />
  <img src="https://github.com/user-attachments/assets/d01f11af-8a1d-4ae0-aee4-084d1e9e0681" alt="Pantalla 2" width="200" />
  <img src="https://github.com/user-attachments/assets/854db213-ce18-468b-a5b7-d41ac98f6f3b" alt="Pantalla 3" width="200" />
  <img src="https://github.com/user-attachments/assets/cca31669-ed82-4d2b-8305-11637e1ed626" alt="Pantalla 4" width="200" />
  <img src="https://github.com/user-attachments/assets/f5a2f02d-fccb-4c0b-8dc6-6fc825b78ea7" alt="Pantalla 5" width="200" />
  <img src="https://github.com/user-attachments/assets/093ecf18-6497-4692-a905-1fd0557cc4c9" alt="Pantalla 6" width="200" />
  <img src="https://github.com/user-attachments/assets/af929108-988a-4940-96ce-e180324e8b4d" alt="Pantalla 7" width="200" />
  <img src="https://github.com/user-attachments/assets/bd7b1c5d-940c-4175-9c0a-541ba1aee76a" alt="Pantalla 8" width="200" />
  <img src="https://github.com/user-attachments/assets/e224bd2c-b652-4150-85a9-8551b1dcced1" alt="Pantalla 9" width="200" />
  <img src="https://github.com/user-attachments/assets/1c83f7f7-9737-4e87-840c-078cc40d41c8" alt="Pantalla 10" width="200" />
  <img src="https://github.com/user-attachments/assets/1c41ceb2-7745-4b7f-84c3-04c699c5e192" alt="Pantalla 11" width="200" />
</div>

🤝 Contribuciones
¡Contribuciones bienvenidas! Para aportar:

Haz un fork del repositorio.

Crea una rama feature/<tu-cambio>.

Envía un pull request describiendo tu aporte.

📄 Licencia
Este proyecto usa la licencia MIT. Consulta LICENSE para más detalles.
