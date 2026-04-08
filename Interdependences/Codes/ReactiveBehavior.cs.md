❌✅
## Fase 1 (Unity Dependency)

using UnityEngine: ✅
using UnityEditor:  ❌

public class NOMBRE : MonoBehaviour ✅

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
Update() : ✅
LateUpdate():
Time.time✅
Random: ✅

## Fase 2 (Strong Dependencies - Composition)

### new

#### Código Proyecto
var aus = new List<VirtualAgent.**ActionUnit**>() [[LoadData.cs]]

new List<Bml.**Signal** [[BML.cs]]

new List<Bml.**Synchro** [[BML.cs]]>
#### Librerías genéricas


### AddComponent


# Fase 3 (Weak Dependencies - Association, Use)

### Caso A 


### Caso B (Inyección por parámetro de función)

public void SetAgent(VirtualAgent.**Character** a) [[Character.cs]]

    {
        agent_ = a;
    }


### Caso D
A ver acá hay algo a remarcar: a nivel scope de lo que ve el código, solo ve "Character.cs". El resto de los otros métodos que vienen en cadena los va a gestionar luego el compilado del proyecto y hay que verificar que estos se cumplan. Sigue esta lógica siempre al parecer:

Character  -> bml_scheduler_behavior -> BML
agent_.**scheduler**[[Character.cs]].Sched.AddBml("blink", Bml.**Composition.MERGE** [[BML.cs]] , new List<Bml.**Signal** [[BML.cs]] >(){
            **SignalBuilder**.**Face** [[bml_scheduler_behavior.cs]](agent_.**scheduler.Sched** , "blink", "blink", 1, false, aus, agent_.**fe** [[FaceEngine.cs]],
                new List<Bml.**Synchro** [[BML.cs]]>(){
                    agent_.scheduler.Sched.NewSynchro("start", "0"),
                    agent_.scheduler.Sched.NewSynchro("ready", "0.25"),
                    agent_.scheduler.Sched.NewSynchro("relax", "0.26"),
                    agent_.**scheduler** [[Character.cs]] .Sched .NewSynchro("end",   "0.51"),
                    }),
            });
    }

# Fase 4 (BehaviorRealizer?)❌

C# puro? ❌
GestureLibrary:  ❌
Time management, BML processing: ❌

