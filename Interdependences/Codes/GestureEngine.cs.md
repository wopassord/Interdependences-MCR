❌✅
## Fase 1 (Unity Dependency)

using UnityEngine: ❌
using UnityEditor:  ❌

public class NOMBRE : MonoBehaviour ❌


#### Buzzwords:❌
Vector3 y Quaternion están definidas internamente. No forman parte de la lógica de Unity

SkinnedMeshRenderer:
GetComponent():
AddComponent():
Instantiate:
GameObject: 
Transform:
Animator:
AudioSource:
Animation:
Vector3:
Vector2:
Quaternion:
Start() : 
Update() : 
LateUpdate():
Time.time

## Fase 2 (Strong Dependencies - Composition)

### new

#### Código Proyecto
List<Bml.Synchro> synchros = new List<**Bml.Synchro**>(sync); [[BML.cs]]



#### Librerías genéricas
nada

### AddComponent
nada

# Fase 3 (Weak Dependencies - Association, Use)

### Caso A 


### Caso B (Inyección por parámetro de función)

internal **Character** agent_; [[Character.cs]]

public void ChangePosture(**Bml.Scheduler** scheduler, **Bml.Event** evt, string stance, string category, [[BML.cs]]
string target, string facing, **PostureDescription** posture, **MocapDescription** mocap)[[LoadData.cs]]

public void PlayGesture(Bml.Scheduler scheduler, Bml.Event evt, string name, string modality, string mode, **GestureDescription** gestureShape_, string target, MocapDescription mocap
[[LoadData.cs]]

### Caso D

# Fase 4 (BehaviorRealizer?)✅

C# puro? ✅
GestureLibrary:  ✅
Time management, BML processing: ✅

Sí, es behavioRealizer

