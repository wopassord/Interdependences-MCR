
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
ttsc = new TextToSpeech.Channel(te_, 0); [[tts.cs]]
fe = new FaceEngine(this) [[FaceEngine.cs]]
toe = new TorsoEngine(this) [[TorsoEngine.cs]]
ge = new GestureEngine(this) [[GestureEngine.cs]]



#### Librerías genéricas
static readonly System.Random random = new System.Random(); [[Random.cs]]
static readonly System.Globalization.CultureInfo ci = new System.Globalization.CultureInfo("en-US"); [[CultureInfo.cs]]
Dictionaries: (one example)
	        internal Dictionary<string, MocapDescription> mocaps_ = new Dictionary<string, MocapDescription>[[Dictionary.cs]];  

System.Xml.XmlTextReader reader = new System.Xml.XmlTextReader(path + name + ".xml"); [[XmlTextReader.cs]]
var signals = new List<Bml.Signal>() [[List.cs]]

### AddComponent

nada

# Fase 3 (Weak Dependencies - Association, Use)

### Caso A 
No hay instancias 

### Caso B (Inyección por parámetro de función)

##### Class Character:
public Animation.IAnimationEngine animationEngine;
public ClientUDP udpClient_;
public BmlSchedulerBehaviour scheduler;
internal TextToSpeech.Engine te_;
internal ReactiveBehavior rb_;


# Fase 4 (BehaviorRealizer?)✅

C# puro? ✅
GestureLibrary:  ✅
Time management, BML processing: ✅
