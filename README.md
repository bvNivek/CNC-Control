# CNC Control - Fase 1 Simulator +  Arquitectura

Proyecto de control CNC con Java - Diseño y simulación

## Fase 1 - Simulator UI
Interfaz con estados CONECTADO/DESCONECTADO, control X/Y/Z, modo CONTINUO/INCREMENTAL, paso 0.1/1.0/10.0, velocidad LENTA/MEDIA/RÁPIDA, STOP, EMERGENCIA, REINICIO, CONECTAR.

## Fase Pro - Arquitectura planeada con Grok
Diseño MVC completo:
- controller: CncController (cerebro), MovementEngine, JogController, SpindleController, OverrideController, SafetyController
- model: Position, MachineState, JogMode, StepSize, CoordinateSystem G54/G55, Tool, SoftLimits
- connection: ConnectionManager COM/baud, SerialPortHandler
- safety: EmergencyStop, FeedHold, AlarmManager
- ui: MainFrame, ControlPanel, StatusPanel, PositionPanel, etc.

Nota: Código en búsqueda, se deja arquitectura y UI como referencia de diseño de sistema embebido.
