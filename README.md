# Reto de Diseño: **AgenticHub – Asistente de Aprendizaje Personalizado**

## Descripción del Reto

**Objetivo:** construir un dashboard interactivo de aprendizaje sobre AgenticAI usando _Vibe Coding_ en [bolt.new](https://bolt.new).  
**Duración:** 45 minutos • **Formato:** equipos de 4–6 personas.  
**Contexto:** la universidad requiere una plataforma divertida y práctica para que estudiantes de nuevo ingreso exploren AgenticAI mediante descripciones en lenguaje natural (sin código específico).

---

## Design Workflows: Múltiples Aproximaciones

### A) Mobile-First Social Learning _(“el Instagram/TikTok del aprendizaje”)_

Crea una app móvil estilo TikTok para aprender AgenticAI:

- Scroll vertical infinito con micro-lecciones de 60 s  
- Cada concepto es un reel interactivo con animaciones  
- Swipe derecho = guardar • Swipe izquierdo = siguiente  
- Doble tap = “me sirvió” + comentarios de dudas  
- Stories de 24 h con retos diarios de prompting  
- Feed personalizado que sugiere repasos  
- Modo dueto: compara tu prompt con el de un experto  
- Notificaciones tipo: “¡Tu amigo dominó RAG! ¿Te unes?”

**Decisiones de usabilidad**  
Patrones familiares (gestos), microlearning bite-size, _social proof_ y FOMO positivo.

---

### B) Desktop Productivity Dashboard _(“el Notion/Obsidian de AgenticAI”)_

Diseña un workspace estilo Notion:

- Kanban de conceptos: **Por aprender → Aprendiendo → Dominado**  
- Grafo de conocimiento interactivo  
- Split screen: teoría (izq.) + playground (der.)  
- Command palette (**Cmd/Ctrl + K**)  
- Editor Markdown con autocompletado de conceptos  
- Widgets: pomodoro, progress tracker, quick quiz  
- Modo zen sin distracciones  
- Sincronización con Calendar para planear sesiones

**Decisiones de usabilidad**  
Power users (atajos), información densa, layout personalizable, foco en productividad.

---

### C) Game-Based PWA _(“Duolingo meets Pokémon”)_

Crea un RPG educativo:

- Avatar “AI Trainer” que colecciona agentes  
- Mapa por regiones (Prompt Plains, RAG Mountains, LangChain City)  
- Batallas por turnos respondiendo correctamente  
- Cada concepto dominado desbloquea un nuevo agente  
- XP, niveles y _skill tree_  
- Daily quests (p. ej., “Crea 3 prompts exitosos”)  
- _Boss battles_ (proyectos complejos multi-concepto)  
- Música 8-bit adaptativa  
- Badges estilo NFT (sin blockchain)

**Decisiones de usabilidad**  
Motivación intrínseca, narrativa, recompensas frecuentes y dificultad adaptativa.

---

## Patrones de Diseño y Componentes Reutilizables

### Component Library sugerida

```javascript
const designSystem = {
  ConceptCard: {
    descripcion: "Tarjeta 3D que gira al hover mostrando ejemplo",
    vibe: "Definición al frente y ejemplo atrás; borde con gradiente luminoso"
  },
  ProgressRing: {
    descripcion: "Anillo circular de progreso con partículas",
    vibe: "Estilo futurista; emite partículas doradas al completar secciones"
  },
  InteractivePromptBox: {
    descripcion: "Editor de prompts con preview en tiempo real",
    vibe: "Vista dividida; syntax highlighting y animación de typing"
  },
  KnowledgeGraph: {
    descripcion: "Visualización 3D de conexiones entre conceptos",
    vibe: "Nodos que pulsan luz; aristas brillan on-hover"
  },
  AIAssistantOrb: {
    descripcion: "Asistente flotante context-aware",
    vibe: "Orbe tipo Jarvis que sigue el cursor y ofrece ayuda con TTS opcional"
  }
};
```

### Micro-interacciones esenciales

1. **Haptic-style feedback:** botones con _press depth_, micro-vibración visual, ripple al clic.  
2. **Carga inteligente:** skeletons con shimmer, mensajes/tips de carga, progress bar que cambia de color según velocidad.  
3. **Transiciones contextuales:** morphing entre vistas, parallax y _stagger_ en listas.  
4. **Feedback de éxito:** confetti con física, _sound FX_ sutiles (whoosh/ding/pop), flash sutil acorde al logro.  
5. **Easter eggs educativos:** Konami code = “modo experto”, tooltips con fun facts al hover prolongado, animaciones especiales en milestones.

---

## Flujos de Usuario Alternativos

### Flow 1: Onboarding Adaptativo

1. **Bienvenida:** “¿Cómo prefieres aprender?” → **Visual / Textual / Hands-on** (adapta el UI).  
2. **Quick Assessment** (3 swipes) → **Novato / Intermedio / Avanzado**.  
3. **Personalización:** tiempo (5/15/30/ilimitado), meta (Aprender/Practicar/Crear), intereses (bubbles).  
4. **Primera victoria rápida:** mini-reto + celebración + primer achievement.

### Flow 2: Learning Path Personalizado (Metro Map)

- Líneas = rutas (Beginner, Advanced Express, Creative)  
- Estaciones = conceptos; intersecciones = cruces multi-área  
- Express routes para saltar contenido dominado  
- “En construcción” para próximos módulos  
- Avatar indica posición actual; siguiente parada recomendada brilla  
- “Ticket de viaje” = progreso del día

### Flow 3: Modo Colaborativo

- Salas de estudio (máx. 6) con pizarra compartida  
- Pair programming de prompts en tiempo real  
- Competencias de velocidad (mejor prompt)  
- Modo profesor (screen-share y explicación)  
- Chat con reacciones/stickers de AgenticAI  
- Sistema de **kudos** y leaderboard semanal

---

## Instrucciones por Fase

### Fase 1 — Ideación Rápida

- Definir sección del curso a gamificar/activar  
- Elegir interacción principal: quiz / chatbot / explorador / simulador  
- Roles:
  - **Vibe Director:** describe funcionalidades  
  - **Prompt Architect:** refina descripciones  
  - **UX Storyteller:** define el flujo  
  - **Demo Master:** arma la demo

### Fase 2 — Vibe Coding en bolt.new

**Prompt inicial sugerido**

```text
Crea una aplicación web moderna y colorida llamada "AgenticHub" que incluya:
- Home con animaciones suaves
- Un dashboard con 4 módulos:
  1) Quiz de fundamentos
  2) Playground de prompts
  3) Visualizador de conceptos RAG con ejemplos
  4) Mini-simulador de flujos LangChain
- Estilo bento grid, colores vibrantes, efectos hover y transiciones smooth
- Sistema de puntos/badges por completar módulos
```

**Iteraciones progresivas**

- Añadir chatbot helper para dudas frecuentes  
- “Conceptos del día” (tarjetas interactivas)  
- Timeline visual del curso  
- “Prompt Battle” para competir en vivo

### Fase 3 — Pulido & Testing

- Afinar UI con descripciones específicas  
- Agregar contenido real del curso  
- Probar interacciones clave  
- Preparar el recorrido de demo

### Fase 4 — Preparación de Demo

- Definir la ruta de presentación  
- Destacar la **feature estrella**  
- Pitch de 30 s

---

## Recursos y Ejemplos

### Banco de prompts de ejemplo

```javascript
// Quiz
const quizData = [
  "¿Qué es un agente en AgenticAI?",
  "Diferencia entre RAG y fine-tuning",
  "¿Cuándo usar LangChain vs. llamadas directas a API?"
];

// Conceptos
const concepts = [
  "Agente", "RAG", "MCP", "Prompt Engineering",
  "Chain of Thought", "Few-shot Learning", "Embeddings"
];

// Flujos LangChain
const workflows = [
  "Pregunta → Búsqueda → Síntesis → Respuesta",
  "Input → Validación → Procesamiento → Output"
];
```

### Vibe Coding Avanzado

**Accesibilidad**

```text
- Switch de alto contraste
- Navegación completa por teclado
- ARIA labels y soporte screen readers
- Textos escalables sin romper layout
- Modo dislexia (tipografías amigables)
- Opción de reducir movimiento
- Captions en video y descripciones de imagen
```

**Performance**

```text
- Lazy loading de imágenes/componentes
- Skeletons durante carga
- Code splitting por rutas
- Service worker (offline)
- Caché de recursos frecuentes
- Debounce en inputs de búsqueda
- Virtual scrolling en listas largas
- Compresión automática de imágenes
```

**Personalización**

```text
- Temas: claro / oscuro / alto contraste / custom
- Tamaño de fuente ajustable
- Velocidad de animaciones configurable
- Layout drag & drop
- Shortcuts definibles por usuario
- Notificaciones configurables
- Idioma y región
- Modo zen sin distracciones
```

---

## Métricas de Usabilidad

```javascript
const metricsToTrack = {
  engagement: {
    timeOnTask: "Tiempo por concepto",
    clickDepth: "Profundidad de exploración",
    returnRate: "Retorno al día siguiente",
    featureUsage: "Herramientas más usadas"
  },
  learning: {
    conceptMastery: "Mejora en quizzes",
    promptQuality: "Evolución de calidad de prompts",
    errorPatterns: "Zonas de confusión",
    helpRequests: "Momentos de solicitud de ayuda"
  },
  satisfaction: {
    rageClicks: "Señales de frustración",
    completionRate: "Tasa de finalización",
    shareRate: "Frecuencia de compartir logros",
    customPaths: "Uso de rutas personalizadas"
  }
};
```

---

## Criterios de Evaluación

| Dimensión | Indicadores | Peso |
|---|---|---|
| **Arquitectura de Información** | Navegación intuitiva; jerarquía clara; _findability_; breadcrumbs efectivos | 20% |
| **Diseño Visual** | Consistencia; accesibilidad (contraste/tamaños); responsive; estética moderna | 20% |
| **Interactividad** | Feedback inmediato; estados hover/active; animaciones con propósito; micro-interacciones | 20% |
| **Pedagogía Digital** | Progresión lógica; _scaffolding_; variedad de formatos; evaluación integrada | 20% |
| **Innovación** | Features únicas; soluciones creativas; uso de IA generativa; _wow factor_ | 20% |

**Bonus (+1 c/u):** Wow visual, meta-learning, gamificación bien integrada, data-viz creativa, personalización en tiempo real.

---

> **Entrega esperada (MVP de demo):**  
> App funcional en bolt.new con al menos **1 workflow** implementado, **1 flujo de usuario** completo, **componentes reutilizables** básicos y **pitch de 30 s** mostrando la _feature estrella_.
