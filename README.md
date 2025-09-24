# Reto de Diseño: **AgenticHub – Asistente de Aprendizaje Personalizado**

![Alt Text](https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExYnByOGd3bzBtaWFncGhtazR3eDVhMndwM3FtanFyNTY5bXVoZXF2dSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/c8NspwwVxwAiA/giphy.gif)


## Descripción del Reto

**Objetivo:** Construir una web/mobile app interactiva de aprendizaje sobre AgenticAI usando _Vibe Coding_ en [bolt.new](https://bolt.new).  
**Duración:** ~60 minutos • **Formato:** equipos de 4 personas.  
**Contexto:** Collective Academy requiere una plataforma lúdica, interactiva y práctica para que nuevos aprendedores/as exploren los conceptos vistos en el curso de AgenticAI. 

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

### Micro-interacciones esenciales

1. **Haptic-style feedback:** botones con _press depth_, micro-vibración visual, ripple al clic.  
2. **Carga inteligente:** skeletons con shimmer, mensajes/tips de carga, progress bar que cambia de color según velocidad.  
3. **Transiciones contextuales:** morphing entre vistas, parallax y _stagger_ en listas.  
4. **Feedback de éxito:** confetti con física, _sound FX_ sutiles (whoosh/ding/pop), flash sutil acorde al logro.  
5. **Easter eggs educativos:** Konami code = “modo experto”, tooltips con fun facts al hover prolongado, animaciones especiales en milestones.

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
JAJAJA Uds tienen que PROMPTEAR
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
