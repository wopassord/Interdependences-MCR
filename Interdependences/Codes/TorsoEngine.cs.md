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
public VirtualAgent.Relative_Torso_Position rtp; [[LoadData.cs]]



### Caso B (Inyección por parámetro de función)

public TorsoEngine(VirtualAgent.Character a) [[Character.cs]]

public void PlayTorso(Bml.**Scheduler** [[BML.cs]] scheduler, Bml.**Event** [[BML.cs]] evt, VirtualAgent.**TorsoShape** [[LoadData.cs]] torso, string lexeme, double amount, string target = "")

private void AddTorsoKeyFrame(List<TorsoKeyFrame keyframes, string n, double t, VirtualAgent.**Relative_Torso_Position** rp, double a) [[LoadData.cs]]

### Caso D

# Fase 4 (BehaviorRealizer?)✅

C# puro? ✅
GestureLibrary:  ✅
Time management, BML processing: ✅

