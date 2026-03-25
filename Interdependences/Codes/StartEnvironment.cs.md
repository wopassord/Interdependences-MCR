## Fase 1 (Unity Dependency)

using UnityEngine: ✅
using UnityEditor: ✅

public class StartEnvironment : MonoBehaviour: ✅

GameObject: ✅
foreach (GameObject vh in GameObject.FindGameObjectsWithTag ("VirtualHuman"))
(BÚSQUEDA EN ESCENA DE UNITY)

Start() : ✅
Update() : ✅


## Fase 2 (Strong Dependencies - Composition)

### new

#### Librerías genéricas
public Dictionary<string, VirtualAgent.Character> agents = new Dictionary<string, VirtualAgent.Character> (); [[System.Collections.Generic]]


#### Código Proyecto
Engine te = new Engine(Application.streamingAssetsPath + "\\cereproc\\voices_48k", delegate (string msg) [[cerevoice_eng.cs]] (NO ENTIENDO AQUÍ QUE ES EL OBJETO ENGINE)


udpClient = new ClientUDP() [[UdpClient.cs]]

VirtualAgent.Character a = new VirtualAgent.Character(vh.name, ae, te, bmlScheduler, rb, udpClient, delegate (string msg)  [[Character.cs]]

using (var streamReader = new System.IO.StreamReader(Application.streamingAssetsPath + "\\xml\\test2.xml", System.Text.Encoding.UTF8)) [[StreamReader.cs]]

### AddComponent

instanciación fuerte de scripts nativa de unity

Animation.UnityAnimationEngine ae = vh.AddComponent<Animation.UnityAnimationEngine>(); [[UnityAnimationEngine.cs]]

BmlSchedulerBehaviour bmlScheduler = vh.AddComponent<BmlSchedulerBehavior<()[[bml_scheduler_behavior.cs]]

ReactiveBehavior rb = vh.AddComponent<ReactiveBehavior<();
[[ReactiveBehavior.cs]]


# Fase 3 (Weak Dependencies - Association, Use)
Dependencia a nivel compilación, aunque no se utilice en el código, este no compila si no logra hacer el vínculo con la clase que se llama. Otras clases eran débiles pero se transforman en fuertes al ser instanciadas

public GestureCreator gc; [[GestureEditor.cs]]

public HandShapeCreator hsc; [[HandShapeEditor.cs]]


# Fase 4 (BehaviorRealizer?)

No depende de Unity? ❌
No es Behavior Realizer entonces
