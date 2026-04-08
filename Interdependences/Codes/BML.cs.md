En este habita la clase "Scheduler" este es el cerebro que se encarga de comunicarse con todos los motores, recibe el delta de tiempo pasado entre la simulación y el tiempo real del clock interno del update del bml_scheduler_behavior y va disparando aquellos comandos que estén en la cola de "Signals" según el tiempo que haya transcurrido para hacer una simulación que vaya a tiempo real. 

❌✅
## Fase 1 (Unity Dependency)

using UnityEngine: ❌
using UnityEditor:  ❌

public class NOMBRE : MonoBehaviour ❌

#### Buzzwords:

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
nada

### Caso B (Inyección por parámetro de función)
nada
### Caso D
nada

# Fase 4 (BehaviorRealizer?)✅

C# puro? ✅
GestureLibrary:  ✅
Time management, BML processing: ✅

Es behavior Realizer

Re contra independiente de todo.