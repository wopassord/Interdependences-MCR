❌✅
## Fase 1 (Unity Dependency)

using UnityEngine: ❌
using UnityEditor:  ❌

public class NOMBRE : MonoBehaviour 

#### Buzzwords:

SkinnedMeshRenderer:
GetComponent():
AddComponent():
Instantiate:
GameObject: 
Transform:
Animator:
AudioSource:
Animation:✅ (duda aquí, es el namespace de un archivo, no es de unity)
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

new **ActionUnit** [[LoadData.cs]]

 headDirections_[s].Add(new **HeadDirectionPhase** [[UnityAnimationEngine.cs]]

#### Librerías genéricas
ignoramos

### AddComponent

nada
# Fase 3 (Weak Dependencies - Association, Use)

### ~~Caso A~~  (NO HAY CASO A SIN UNITY)


### Caso B (Inyección por parámetro de función)



internal **Character** agent_; [[Character.cs]]

float start = (float)evt.**Signal**.FindSynchro("start").Time; [[BML.cs]]

public void PlayHead(Bml.**Schedule**r scheduler, Bml.**Event** evt, HeadShape head, int repetition, double amount, string target) [[BML.cs]]


public void PlaySpeech(Bml.Scheduler scheduler, Bml.Event evt, TextToSpeech.**SpeechData** sdata) [[tts.cs]]

### Caso D


# Fase 4 (BehaviorRealizer?)
C# puro? ✅
GestureLibrary:  ✅
Time management, BML processing: ✅

Es BehaviorRealizer