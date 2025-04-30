# Componentes de un Agente de IA en n8n

Este diagrama conceptual describe los componentes clave de un agente de Inteligencia Artificial (IA) implementado utilizando la plataforma de automatización n8n, junto con sus conectores y el flujo general del proceso.

```mermaid
graph LR
    A[Entrada (Input)] --> B(Percepción);
    subgraph Triggers n8n
        style A fill:#f9f,stroke:#333,stroke-width:2px
        A1[Email (IMAP)]
        A2[Base de Datos]
        A3[Webhook]
        A4[Aplicación SaaS]
        A5[Cron]
        A --> A1 & A2 & A3 & A4 & A5
    end

    B --> C(Procesamiento y Razonamiento);
    subgraph Nodos de Transformación n8n
        style B fill:#ccf,stroke:#333,stroke-width:2px
        B1[Function (JavaScript)]
        B2[JSON Parse]
        B3[String Manipulation]
        B4[API Request]
        B --> B1 & B2 & B3 & B4
    end

    C --> D[Acción (Action)];
    subgraph Nodos de Lógica y IA n8n
        style C fill:#9cf,stroke:#333,stroke-width:2px
        C1[If]
        C2[Switch]
        C3[Set]
        C4[Loop]
        C5[Integración IA (OpenAI, Google Cloud AI)]
        C --> C1 & C2 & C3 & C4 & C5
    end

    D --> E[(Memoria (Opcional))];
    subgraph Nodos de Integración n8n
        style D fill:#fcc,stroke:#333,stroke-width:2px
        D1[Email Send]
        D2[Base de Datos]
        D3[HTTP Request]
        D4[Messaging Apps]
        D5[CRM]
        D --> D1 & D2 & D3 & D4 & D5
    end

    subgraph Almacenamiento de Memoria n8n
        style E fill:#efe,stroke:#333,stroke-width:2px
        E1[Variables de Entorno]
        E2[Bases de Datos Externas]
        E3[Servicios de Almacenamiento]
        E4[Nodos de Espera/Respuesta]
        E -- Almacena/Recupera --> E1 & E2 & E3 & E4
        C -- Toma Decisiones Basadas en --> E
    end

    subgraph Flujo General del Proceso
        F[Trigger Activa el Flujo] --> G(Procesamiento de Datos);
        G --> H{¿Condición Cumplida?};
        H -- Sí --> I[Ejecutar Acción];
        H -- No --> J[Otro Proceso/Fin];
        I --> K[Fin del Flujo (o Continúa)];
    end
