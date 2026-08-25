# RAVA S.A. — Plataforma Corporativa de Capacitación en Inteligencia Artificial

Plataforma web interactiva de formación y capacitación corporativa en Inteligencia Artificial y Agentes Autónomos para los colaboradores y directivos de **RAVA S.A.** (Vialidad, Infraestructura Vial, Compras, Obras y Logística).

**Desarrollado y Dictado por:** Brian Ruiz Moreno & León Schwegler  
**Edición:** 2026

---

## 🧭 Estructura y Módulos de la Plataforma

La plataforma se organiza en dos módulos de capacitación complementarios y de acceso directo:

```text
├── index.html        # Módulo 2: Prompt Engineering & Automatización Práctica
├── agente/
│   ├── index.html    # Módulo 3: Agentes Autónomos, Arquitectura ReAct y Skills
│   └── assets/       # Recursos gráficos y branding
├── assets/           # Logos e íconos compartidos
└── README.md         # Documentación técnica y pedagógica
```

---

## 📚 Módulo 2: Prompt Engineering Aplicado al Entorno Corporativo (`index.html`)

Enfocado en la formulación de instrucciones de alto rendimiento para el trabajo diario:

1. **Introducción a la IA Generativa:** Aplicaciones reales en vialidad y obra (resúmenes de pliegos, estructuración de informes y detección de inconsistencias).
2. **La Anatomía de un Prompt Profesional:** Los 6 componentes esenciales (Rol, Tarea, Contexto, Razonamiento, Formato de Salida y Condición de Fin).
3. **Frameworks Estándar de la Industria:**
   - **CO-STAR:** Contexto, Objetivo, Estilo, Tono, Audiencia, Respuesta (tareas de alto impacto y reportes ejecutivos).
   - **RTF:** Rol, Tarea, Formato (operaciones rápidas del día a día).
   - **RISEN:** Rol, Instrucciones, Secuencia, Entregable, Negativas (procesos técnicos con restricciones estrictas).
4. **Técnicas Avanzadas:** Delimitadores XML, *Few-Shot*, *Chain-of-Thought* y *Self-Verification*.
5. **Comparador Interactivo «Antes vs. Después»:** Casos de uso reales segmentados por área de RAVA S.A. (Administración, Compras, RRHH, Taller, Técnicos y Dirección).
6. **Generador Dinámico de Prompts + Biblioteca:** Herramienta interactiva con vista previa y copiado al portapapeles.
7. **Gobernanza y Reglas de Oro:** *Garbage In = Garbage Out*, Supervisión Humana Obligatoria (*Human-in-the-Loop*) y Confidencialidad de Datos.

---

## 🤖 Módulo 3: Agentes Autónomos y Arquitectura de Skills (`agente/index.html`)

Enfocado en la transición de un chatbot conversacional a un **Agente Autónomo** capaz de ejecutar tareas multi-paso, interactuar con herramientas y auto-corregirse ante desvíos.

### 1. La Diferencia Fundamental
- **Chatbot:** Devuelve texto y sugerencias; el usuario debe ejecutar el trabajo manualmente.
- **Agente con Skills:** Razona, descompone la meta en tareas, ejecuta herramientas reales y entrega el trabajo verificado.

### 2. El Ciclo de Vida en Seis Pasos
1. **Recibe:** Captura el objetivo y recupera el contexto de memoria.
2. **Planifica:** Descompone la meta y activa la Skill procedimental requerida.
3. **Elige:** Selecciona las herramientas digitales adecuadas (OCR, ERP, planillas, cronogramas).
4. **Ejecuta:** Aplica las acciones y lee el resultado real de cada sistema.
5. **Corrige:** Identifica errores o desvíos, ajusta la estrategia y reintenta dentro del bucle.
6. **Entrega:** Consolida resultados, deja trazabilidad en bitácora y solicita aprobación humana para acciones críticas.

### 3. Las Seis Piezas Esenciales de un Agente

| Pieza | Función Técnica | Analogía RAVA S.A. | Si Falta... |
| :--- | :--- | :--- | :--- |
| **Objetivo** | Meta cuantificable a lograr | El destino del taxi | Da vueltas en círculos y devuelve texto vago. |
| **Instrucciones** | Guardrails y límites fijos | Reglamento de tránsito y seguridad de obra | Borra archivos o compromete datos sin permiso. |
| **Memoria** | Historial y variables persistentes | Bitácora y libro diario de obra | Hay que repetir el contexto en cada interacción. |
| **Herramientas** | Interfaces hacia ERP, OCR, APIs | Kit de llaves y maquinaria del taller | Solo opina: es un chatbot tradicional sin manos. |
| **Skills** | Manual de procedimiento y método experto | Protocolo técnico DNV de pavimentación | Improvisa los pasos y saltea validaciones críticas. |
| **El Bucle** | Capacidad ReAct de corregirse y reintentar | Ajustar la llave hasta que encaje | Se rinde ante el primer error inesperado. |

---

## 🧩 ¿Qué es una Skill y cómo opera a nivel empresarial?

Una **Skill** es un paquete modular de conocimiento procedimental y heurístico empaquetado bajo demanda (*Progressive Disclosure*). En lugar de saturar la memoria del agente con cientos de manuales, el agente solo carga el procedimiento específico cuando el usuario solicita una tarea que lo requiere.

### Casos de Uso Implementados en RAVA S.A.:
* **Skill de Auditoría de Remitos vs. OC:** Extrae peso bruto, tara y neto por OCR, cruza con la Orden de Compra en el ERP Physis y aplica la tolerancia admisible de $\pm 2\%$ por humedad de cantera.
* **Skill de Despiece de Pliegos Licitatorios:** Extrae equipo mínimo exigido, fórmula polinómica de reajuste y detecta penalidades por mora.
* **Skill de Rendimiento de Maquinaria:** Cruza partes diarios de choferes, calcula ratios $\text{Litros/Hora}$ y emite alertas preventivas ante desvíos mayores al $15\%$.

---

## 🛠️ Stack Tecnológico & Arquitectura Web

- **HTML5 Semántico & CSS3 Moderno:** Variables CSS (Design Tokens), animaciones aceleradas por GPU (`transform`, `opacity`), tipografía Manrope + Inter/Poppins.
- **Micro-interacciones Fluidas:** Reproductor interactivo, tarjetas 3D con efecto flip (`preserve-3d`), órbita SVG con respiración y tilt interactivo.
- **Simulador de Consola ReAct:** Visualización en vivo de fases del bucle, reintentos y generación reactiva de resultados.
- **Quiz de Validación & Gamificación:** Feedback dinámico inmediato, cálculo de métricas y animación de confetti.
- **Persistencia Local:** Checklist interactivo sincronizado en `localStorage` (`mpa-ck`).
- **Accesibilidad & Responsive:** Compatible con WCAG 2.1 AA (ratios de contraste $>4.5:1$, navegación por teclado `:focus-visible`, soporte `prefers-reduced-motion` y adaptabilidad completa de 360px a 4K).

---

## 🚀 Puesta en Marcha

La plataforma está diseñada como una aplicación web estática sin dependencias de servidor:

1. Clonar o abrir la carpeta del repositorio:
   ```bash
   git clone <repo-url>
   ```
2. Abrir `index.html` (Módulo de Prompt Engineering) o `agente/index.html` (Módulo de Agentes) directamente en cualquier navegador web moderno (Chrome, Edge, Firefox, Safari).
3. No requiere compilación, Node.js ni servidor backend para su funcionamiento visual e interactivo.

---

## 📄 Propiedad Intelectual & Licencia

Material de capacitación técnica interna desarrollado exclusivamente para **RAVA S.A.** — Todos los derechos reservados © 2026.
