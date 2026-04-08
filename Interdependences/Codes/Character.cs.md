
## Fase 1 (Unity Dependency)

using UnityEngine: ❌ (commenté)
using UnityEditor:  ❌

public class NOMBRE : MonoBehaviour ❌

Buzzwords: ❌
GameObject: ❌

Start() : ❌
Update() : ❌



## Fase 2 (Strong Dependencies - Composition)

### new

#### Código Proyecto
##### Class Character:
ttsc = new TextToSpeech.**Channel**(te_, 0); [[tts.cs]]
fe = new **FaceEngine**(this) [[FaceEngine.cs]]
toe = new **TorsoEngine**(this) [[TorsoEngine.cs]]
ge = new **GestureEngine**(this) [[GestureEngine.cs]]

new **ActionUnit** [[LoadData.cs]]



### AddComponent

nada

# Fase 3 (Weak Dependencies - Association, Use)

### Caso A 
No hay instancias 

### Caso B (Inyección por parámetro de función)

##### Class Character:
public Animation.IAnimationEngine animationEngine; [[UnityAnimationEngine.cs]] [[IAnimationEngine.cs]]
public ClientUDP udpClient_; [[UdpClient.cs]]
public BmlSchedulerBehaviour scheduler; [[BML.cs]]
internal TextToSpeech.Engine te_; [[tts.cs]]
internal ReactiveBehavior rb_; [[ReactiveBehavior.cs]]


# Fase 4 (BehaviorRealizer?)✅

C# puro? ✅
GestureLibrary:  ✅
Time management, BML processing: ✅
