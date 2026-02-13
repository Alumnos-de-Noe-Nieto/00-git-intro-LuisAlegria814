# 2️⃣A ¿Qué es Git? - Los 3 Conceptos Clave

⏱️ **Tiempo recomendado:** 12 minutos

**Objetivo:** Entender qué ES Git (no cómo usarlo aún).

---

## La Historia que Todos Vivimos

Tu profesor te pide hacer un proyecto en equipo con 3 compañeros. Van a programar un videojuego juntos. El proyecto tiene 5 archivos:
- `main.py` - programa principal
- `jugador.py` - clase del jugador
- `enemigos.py` - clase de enemigos
- `pantalla.py` - dibujo de gráficos
- `sonidos.py` - efectos de sonido

¿Cómo colaborarían sin Git?

---

## 🔴 El Caos sin Git

### El Problema Real

```
📁 Proyecto Final
  ├── main.py (versión Paula)
  ├── main.py (versión Carlos)
  ├── main.py (ULTIMA VERSION)
  ├── jugador.py (no tocar)
  ├── jugador.py.bak
  ├── enemigos.py
  └── README (POR FAVOR LEE ESTO PRIMERO).txt
```

**¿Cuáles son los problemas?**

| Problema | Lo que sucede |
|----------|-----------|
| 🤔 **¿Cuál es la versión correcta?** | ¿Es `main.py (versión Paula)` o `main.py ULTIMA VERSION`? |
| 💔 **Cambios perdidos** | Paula modifica `jugador.py`, pero Carlos sobrescribe su trabajo sin darse cuenta |
| 🔄 **Imposible de fusionar** | Laura y Francisco modifican el mismo archivo al mismo tiempo |
| ⏰ **Sin historial** | No sé qué cambió, cuándo cambió ni por qué |
| 🐛 **Algo se rompió!** | ¿Cuál fue el cambio que rompió el programa? Tengo que revisar TODO |

---

## 🟢 La Solución: Git

Git es un **sistema de control de versiones** — piénsalo como una "máquina del tiempo" para tu código.

**Git te permite:**

✅ **Un único repositorio central** — un lugar único donde están TODOS los archivos

✅ **Historial completo** — puedes ver qué cambió, cuándo y quién lo hizo

✅ **Revertir cambios** — si algo se rompe, vuelves al código anterior (es como un save point)

✅ **Colaboración sin conflictos** — varios compañeros trabajan sin pisar cambios del otro

---

## 🎓 Los 3 Conceptos Clave

Para entender Git, necesitas solo ESTOS 3:

### 1. **Repositorio** 📦
Tu proyecto completo. Es una carpeta "especial" que Git vigila.

```
Mi Proyecto/
├── .git/              ← Aquí Git guarda toda la historia
├── main.py
├── jugador.py
├── enemigos.py
└── pantalla.py
```

**¿Qué es `.git`?** Una carpeta invisible donde Git almacena:
- Todos los cambios que hiciste
- Quién hizo cada cambio
- Cuándo se hizo cada cambio
- Mensajes describiendo por qué

---

### 2. **Commit** 💾
Un "punto de guardado" en tu código.

```
Cuando terminas algo funcional:

ANTES:  main.py sin menú
↓
[Trabajas 10 minutos]
↓
DESPUÉS: main.py con menú

Git registra: "Paula agregó menú principal"
ID único: a3f8c2
Hora: Hoy 3:30 PM
```

Un commit es:
- **Qué cambió** — los archivos modificados
- **Quién lo hizo** — Paula, Carlos, Laura, etc.
- **Cuándo pasó** — fecha y hora exacta
- **Por qué pasó** — un mensaje descriptivo
- **ID único** — para identificarlo siempre

---

### 3. **Rama** 🌳
Una "línea de desarrollo" separada del trabajo principal.

```
main (la rama oficial, siempre debe funcionar)
  ↓
feature-menu (donde Paula trabaja en menú)
  ↓
feature-enemigos (donde Carlos trabaja en enemigos)
```

**¿Por qué ramas?**
- Cada quien trabaja en su propia rama
- No interfi
eren en el trabajo del otro
- Cuando terminan, se fusionan en `main`

---

## ¿Qué es un Commit? (El Corazón de Git)

Imagina que cada commit es como un "screenshot" de tu proyecto en un momento específico:

```
Commit 1: "Crear archivos iniciales"
├── main.py (5 líneas)
├── jugador.py (10 líneas)
└── enemigos.py (0 líneas) ← vacío
Hora: 9:00 AM

Commit 2: "Implementar clase Jugador"
├── main.py (5 líneas) ← sin cambios
├── jugador.py (50 líneas) ← modificado
└── enemigos.py (0 líneas) ← sin cambios
Hora: 11:30 AM

Commit 3: "Agregar enemigos"
├── main.py (5 líneas) ← sin cambios
├── jugador.py (50 líneas) ← sin cambios
└── enemigos.py (35 líneas) ← nuevo contenido
Hora: 2:00 PM
```

Git puede ir hacia ATRÁS en tiempo: "Quiero el código de las 11:30 AM" → ✅ Lo hace instantáneamente.

---

## ✅ Checkpoints: Los Conceptos Básicos

### Checkpoint 1: Entiendes el Problema ✅

- [X] Leo: "El Caos sin Git"
- [X] **Verificación:** Piensa en el problema real:
  - "¿Cómo colaborarían 4 compañeros sin Git?"
  - Escribe al menos 1 problema en tu mente (ej: sobrescribir archivos)
- [X] Si pensaste en al menos 1 → ✅ Marca este checkpoint

### Checkpoint 2: Entiendes la Solución ✅

- [X]] Leo: "La Solución: Git"
- [X] **Verificación:** Responde sin mirar el documento:
  - "¿Git es un programa local o en la nube?"
  - **Respuesta correcta:** "Local (en tu computadora)"
- [X] Si respondiste correctamente → ✅ Marca este checkpoint

### Checkpoint 3: Los 3 Conceptos Cristal Claros ✅

- [X] Leo: Las definiciones de Repositorio, Commit, Rama
- [X] **Verificación:** Completa estas frases:
  - "Un repositorio es..." → `[tu carpeta + la carpeta .git]`
  - "Un commit es..." → `[un punto de guardado con cambios]`
  - "Una rama es..." → `[una línea de desarrollo]`
- [X] Si completaste correctamente las 3 → ✅ Marca este checkpoint

---

## 💾 Guarda tu Progreso

Ahora que completaste esta lección y marcaste todos los checkpoints, ejecuta estos comandos para guardar tu progreso en un commit y que el autograder te lo califique cuando hagas push.

```bash
git add docs/02-QUE-ES-GIT.md
git commit -m "Completo 02: Conceptos clave de Git"
```

**Confirmación:** En tu terminal deberías ver:

```
[main xxxxxxx] Completo 02: Conceptos clave de Git
 1 file changed, [X] insertions(+), [Y] deletions(-)
```

---

## 🔗 Navegación

← [Anterior: Instalación](./01-INSTALACION.md) 

→ [Siguiente: Por Qué Git Importa](./03-POR-QUE-GIT.md)
