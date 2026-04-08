```mermaid
classDiagram
    %% 1. Definición de Paletas de Colores (Leyenda)
    classDef CsharpPuro fill:#1e4620,stroke:#4caf50,stroke-width:2px,color:#fff;
    classDef UnityDep fill:#5c1a1a,stroke:#f44336,stroke-width:2px,color:#fff;
    classDef Periferico fill:#1c2d54,stroke:#2196f3,stroke-width:2px,color:#fff;

    %% 2. Declaración de Nodos y Categorización
    class LoadData:::CsharpPuro
    class BML:::CsharpPuro
    class Character:::CsharpPuro
    class FaceEngine:::CsharpPuro
    class GestureEngine:::CsharpPuro
    class TorsoEngine:::CsharpPuro
    class IAnimationEngine:::CsharpPuro
    class synchro_solver:::CsharpPuro

    class bml_scheduler_behavior:::UnityDep
    class UnityAnimationEngine:::UnityDep
    class ReactiveBehavior:::UnityDep
    class StartEnvironment:::UnityDep

    class tts:::Periferico
    class UdpClient:::Periferico

    %% 3. Relaciones de Implementación (Interfaces)
    UnityAnimationEngine ..|> IAnimationEngine : Implementa

    %% 4. Dependencias Fuertes (Composición *-- )
    Character *-- tts : new()
    Character *-- FaceEngine : new()
    Character *-- TorsoEngine : new()
    Character *-- GestureEngine : new()
    Character *-- LoadData : new()
    
    bml_scheduler_behavior *-- BML : new()
    
    FaceEngine *-- LoadData : new()
    
    GestureEngine *-- BML : new Synchro()
    
    ReactiveBehavior *-- LoadData : new()
    ReactiveBehavior *-- BML : new()
    
    StartEnvironment *-- tts : new Engine()
    StartEnvironment *-- UdpClient : new ClientUDP()
    StartEnvironment *-- Character : new()
    StartEnvironment *-- UnityAnimationEngine : AddComponent()
    StartEnvironment *-- bml_scheduler_behavior : AddComponent()
    StartEnvironment *-- ReactiveBehavior : AddComponent()

    %% 5. Dependencias Débiles (Asociación/Uso --> )
    Character --> IAnimationEngine : Inyectado
    Character --> UdpClient : Inyectado
    Character --> bml_scheduler_behavior : Inyectado
    Character --> tts : Inyectado
    Character --> ReactiveBehavior : Inyectado

    bml_scheduler_behavior --> FaceEngine : Parámetro/Uso
    bml_scheduler_behavior --> tts : Parámetro/Uso
    bml_scheduler_behavior --> BML : Parámetro/Uso
    bml_scheduler_behavior --> synchro_solver : Parámetro/Uso
    bml_scheduler_behavior --> LoadData : Parámetro/Uso
    bml_scheduler_behavior --> GestureEngine : Parámetro/Uso
    bml_scheduler_behavior --> TorsoEngine : Parámetro/Uso

    FaceEngine --> Character : Inyectado
    FaceEngine --> BML : Parámetro/Uso
    FaceEngine --> tts : Parámetro/Uso

    GestureEngine --> Character : Inyectado
    GestureEngine --> BML : Parámetro/Uso
    GestureEngine --> LoadData : Parámetro/Uso

    TorsoEngine --> Character : Inyectado
    TorsoEngine --> BML : Parámetro/Uso
    TorsoEngine --> LoadData : Parámetro/Uso

    UnityAnimationEngine --> Character : Inyectado/Uso
    UnityAnimationEngine --> tts : Inyectado/Uso
    UnityAnimationEngine --> LoadData : Inyectado/Uso
    UnityAnimationEngine --> GestureEngine : Uso interno

    ReactiveBehavior --> Character : Inyectado
    ReactiveBehavior --> bml_scheduler_behavior : Uso encadenado
    ReactiveBehavior --> FaceEngine : Uso encadenado

    synchro_solver --> BML : Parámetro

    IAnimationEngine --> Character : Dependencia de Interfaz
    IAnimationEngine --> tts : Dependencia de Interfaz
    IAnimationEngine --> LoadData : Dependencia de Interfaz
