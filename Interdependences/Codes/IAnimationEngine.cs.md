❌✅
## Fase 1 (Unity Dependency)

using UnityEngine: ❌
using UnityEditor:  ❌

public class NOMBRE : MonoBehaviour ❌

#### Buzzwords:❌

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
nada
#### Librerías genéricas
nada

### AddComponent
nada

# Fase 3 (Weak Dependencies - Association, Use)

### Caso A 

### Caso B (Inyección por parámetro de función)
void SetAgent(VirtualAgent.**Character** a); [[Character.cs]]
void PlayVoice(TextToSpeech.SpeechData sdata); [[tts.cs]]
**VirtualAgent.Vector3** FindJointPosition(string name); [[LoadData.cs]]


### Caso D

# Fase 4 (BehaviorRealizer?)❌

C# puro? ✅
GestureLibrary:  ❌
Time management, BML processing: ❌

NO ES BEHAVIOR REALIZER

Es sólo una una interfaz (UML concept) que va a trabajar a nivel de compatibilidad de compilación únicamente. Si una función espera un objeto que fue definido con una interfaz, entonces el objeto enviado debe cumplir con los métodos y atributos que defina la interfaz (como condición mínima, luego puede agregar lo que quiera el objeto). Maneja un tema de compatibilidades