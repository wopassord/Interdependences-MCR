❌✅
## Fase 1 (Unity Dependency)

using UnityEngine: ✅
using UnityEditor:  

public class NOMBRE : MonoBehaviour ✅
    
    public class UnityAnimationEngine : MonoBehaviour, IAnimationEngine
#### Buzzwords: 
SkinnedMeshRenderer:✅
GetComponent():✅
AddComponent():✅
Instantiate:✅
GameObject: ✅
Transform:✅
Animator:✅
AudioSource:✅
Animation:✅
Vector3:✅
Vector2:✅
Quaternion:✅
Start() : ✅
Update() : ✅
LateUpdate():✅
Time.time✅

## Fase 2 (Strong Dependencies - Composition)

### new

#### Código Proyecto

animatorOverrideController = new AnimatorOverrideController(); [UnityEngine](UnityEngine)

  BipedReferences references = new BipedReferences(); [FinalIK](FinalIK) (no estoy seguro)
#### Librerías genéricas
float
Tuple
CultureInfo
XmlTextReader

### AddComponent
audioS = gameObject.AddComponent<AudioSource();
ik = gameObject.AddComponent<FullBodyBipedIK();
 lookAt = gameObject.AddComponent<LookAtIK();
# Fase 3 (Weak Dependencies - Association, Use)

### Caso A 

### Caso B (Inyección por parámetro de función)

public void SetAgent(VirtualAgent.Character a)
{
	agent_ = a;
}[Character.cs](Character.cs)

private Quaternion GetUnityQuaternion(VirtualAgent.Quaternion rotation)
{
	return new Quaternion(rotation.x, rotation.y, rotation.z, rotation.w);
} [LoadData.cs](LoadData.cs)


### Caso B (Declaración dentro de clase)

internal VirtualAgent.Character agent_; [Character.cs](Character.cs)
public void PlayVoice(TextToSpeech.SpeechData sdata) [tts.cs](tts.cs)

private GestureKeyFrame SetHand(VirtualAgent.HandKeyFrame kframe, char side, VirtualAgent.HandKeyFrame posture = null) [GestureEngine.cs](GestureEngine.cs)

private void moveArm(List<VirtualAgent.HandKeyFrame> frames, double time, char side)[GestureEngine.cs](GestureEngine.cs) 

### Caso D


# Fase 4 (BehaviorRealizer?)
