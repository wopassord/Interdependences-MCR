❌✅

FINALMENTE NO SE OCUPA NADA DE LA SINCRONIZACIÓN, esta tarea la ocupa el [BML.cs](BML.cs)
Funciones principales:
- Wrapping de las órdenes en paquetes lógicos (Signals) con los tiempos de inicio, punto máximo y final, para gestionar cada aspecto del agente, cara, voz, gestos, torso,etc.
- Va llevando un timer del tiempo pasado en el mundo real y le va actualizando al cerebro verdadero Bml.Scheduler de BML.cs cuanto tiempo ha pasado. 
- BML.cs hace la 
## Fase 1 (Unity Dependency)✅
SALVEDAD: En el código está comentado el flag "USING_UNITY3D" (Habría que chequear si se logró el time management sin Unity)

using UnityEngine: ❌
using UnityEditor:  ❌

public class NOMBRE : MonoBehaviour ✅ (FUERA DEL FLAG IF USING UNITY3D, así que sigue siendo dependiente)

**Buzzwords:** 

GameObject: 
Debug:✅
Start() : 
Update() : ✅
Time.time: ✅[UnityEngine](UnityEngine)

## Fase 2 (Strong Dependencies - Composition)

### new

#### Código Proyecto

**Clase BmlSchedulerBehaviour**: instancia de objeto **Scheduler** de BML.cs
sched_ = new **Scheduler**(Time.time, "end", "speech", 0.0, delegate (string msg) [BML.cs](BML.cs)
#### Librerías genéricas

### AddComponent

Nada

# Fase 3 (Weak Dependencies - Association, Use)

### Caso A 

public class Time [UnityEngine](UnityEngine)

### Caso B (Inyección por parámetro de función)

public class SignalBuilder{
 static string Prefix(Scheduler sched, Bml.Event evt) [BML.cs](BML.cs)
}

Signal **Speech**
Namespace VirtualAgent:
- FaceEngine [[FaceEngine.cs]]
Namespace TextToSpeech:
- SpeechData [[tts.cs]]
Namespace Bml:
- Event [BML.cs](BML.cs)

Signal **Gaze**
Namespace VirtualAgent:
- FaceEngine [[FaceEngine.cs]]
Namespace Bml:
- Event [BML.cs](BML.cs)
- SynchroSolver [synchro_solver.cs](synchro_solver.cs.md)

Signal **Face**:
Namespace VirtualAgent:
- ActionUnit [LoadData.cs](LoadData.cs.md)
- FaceEngine [[FaceEngine.cs]]
Namespace Bml:
- Event [BML.cs](BML.cs)
- SynchroSolver [synchro_solver.cs](synchro_solver.cs.md)

Signal **Head**:
Namespace VirtualAgent:
- FaceEngine [[FaceEngine.cs]]
- HeadShape [LoadData.cs](LoadData.cs.md)
Namespace Bml:
- Event [BML.cs](BML.cs)
- SynchroSolver [synchro_solver.cs](synchro_solver.cs.md)

Signal **Gesture**:
Namespace VirtualAgent:
- GestureEngine [GestureEngine.cs](GestureEngine.cs)
- GestureDescription [LoadData.cs](LoadData.cs.md)
- MocapDescription [LoadData.cs](LoadData.cs.md)
Namespace Bml:
- Event [BML.cs](BML.cs)
- SynchroSolver [synchro_solver.cs](synchro_solver.cs.md)

Signal **Pointing**:
Namespace VirtualAgent:
- GestureEngine [GestureEngine.cs](GestureEngine.cs)
- GestureDescription [LoadData.cs](LoadData.cs.md)
Namespace Bml:
- Event [BML.cs](BML.cs)

Signal **Torso**:
[TorsoEngine.cs](TorsoEngine.cs)
Namespace VirtualAgent:
- TorsoShape [LoadData.cs](LoadData.cs.md)
Namespace Bml:
- Event [BML.cs](BML.cs)
- SynchroSolver [synchro_solver.cs](synchro_solver.cs.md)

Signal **Locomotion**:
Namespace Bml:
- Event [BML.cs](BML.cs)

Signal **Posture**:
Namespace VirtualAgent:
- GestureEngine [GestureEngine.cs](GestureEngine.cs)
- PostureDescription [LoadData.cs](LoadData.cs.md)
- MocapDescription [LoadData.cs](LoadData.cs.md)
Namespace Bml:
- Event [BML.cs](BML.cs)
- SynchroSolver [synchro_solver.cs](synchro_solver.cs.md)


# Fase 4 (BehaviorRealizer?) ❌

