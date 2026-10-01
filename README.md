# Venta con criterio

Skill para Codex y Claude orientada a vender automatizaciones y software desde el problema del negocio, el resultado esperado y la evidencia disponible.

Ayuda a convertir información de un prospecto en:

- preguntas de diagnóstico;
- una hipótesis de automatización;
- un cálculo transparente de impacto;
- una oferta comercial;
- un razonamiento de precio;
- una propuesta de instalación y servicio mensual;
- un plan inicial de captación y demostración.

La skill evita completar datos inexistentes, copiar precios de ejemplo o convertir estimaciones en resultados garantizados.

## Estructura

```text
venta-con-criterio/
├── SKILL.md
├── references/
│   ├── fundamentos-y-diagnostico.md
│   ├── oferta-precio-y-entregables.md
│   └── soluciones-y-adquisicion.md
└── evals/
    └── evals.json
```

`SKILL.md` contiene el flujo principal. Las referencias amplían únicamente el modo de trabajo que corresponda a cada pedido.

## Instalación

### Opción recomendada: una copia para Codex y Claude Code

Esta opción mantiene una sola copia del repositorio y la enlaza desde los directorios personales de ambos clientes.

1. Creá los directorios necesarios:

   ```bash
   mkdir -p ~/.agents/skills ~/.codex/skills ~/.claude/skills
   ```

2. Cloná la skill:

   ```bash
   git clone https://github.com/godoylucase/venta-con-criterio.git ~/.agents/skills/venta-con-criterio
   ```

3. Enlazala para Codex y Claude Code:

   ```bash
   ln -s ~/.agents/skills/venta-con-criterio ~/.codex/skills/venta-con-criterio
   ln -s ~/.agents/skills/venta-con-criterio ~/.claude/skills/venta-con-criterio
   ```

4. Verificá que ambos clientes puedan encontrar `SKILL.md`:

   ```bash
   test -f ~/.codex/skills/venta-con-criterio/SKILL.md
   test -f ~/.claude/skills/venta-con-criterio/SKILL.md
   ```

5. Iniciá una sesión nueva en el cliente que vayas a usar.

### Instalar únicamente en Codex

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/godoylucase/venta-con-criterio.git ~/.codex/skills/venta-con-criterio
```

Después, iniciá una sesión nueva. Podés invocarla explícitamente como `$venta-con-criterio` o dejar que Codex la seleccione cuando el pedido coincida con su descripción.

### Instalar únicamente en Claude Code

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/godoylucase/venta-con-criterio.git ~/.claude/skills/venta-con-criterio
```

Después, iniciá una sesión nueva. Podés invocarla explícitamente como `/venta-con-criterio` o dejar que Claude la seleccione cuando el pedido coincida con su descripción.

### Actualizar la instalación

Si usaste la opción compartida:

```bash
git -C ~/.agents/skills/venta-con-criterio pull --ff-only
```

Si la instalaste directamente en un solo cliente, reemplazá la ruta por `~/.codex/skills/venta-con-criterio` o `~/.claude/skills/venta-con-criterio`.

Las rutas utilizadas siguen la documentación de [skills en Codex](https://developers.openai.com/blog/eval-skills) y [skills en Claude Code](https://code.claude.com/docs/en/skills). Claude Code admite que la carpeta de una skill sea un enlace simbólico.

## Ejemplos de uso

- “Un prospecto dice que necesita un chatbot. Ayudame a diagnosticar antes de ofrecerle algo.”
- “Convertí este flujo de seguimiento y agendamiento en una oferta comercial.”
- “Tengo estos costos y esta estimación de horas ahorradas. Ayudame a razonar el precio.”
- “Todavía no tengo casos. Diseñame una secuencia para conseguir los primeros interesados.”

## Origen y créditos

Esta es una adaptación independiente construida a partir de aprendizajes obtenidos en [Triple A](https://www.skool.com/tripleai?utm_source=skooldotcom&utm_campaign=user_profile_page), comunidad y formación sobre inteligencia artificial, automatizaciones y venta de servicios.

El crédito por el material formativo original, sus clases, ejemplos y recursos corresponde a Triple A y a sus autores. Si querés acceder al contenido original y actualizado, hacelo desde su comunidad oficial.

Este repositorio:

- no está afiliado, patrocinado ni aprobado por Triple A;
- no contiene audios, videos, transcripciones, plantillas ni recursos descargables del curso;
- no pretende reemplazar la formación original;
- comparte una síntesis independiente transformada en instrucciones para agentes.

Consultá también [NOTICE.md](NOTICE.md).

## Evidencia y límites

Las fórmulas y catálogos incluidos sirven para formular hipótesis. Una respuesta generada con la skill debe distinguir datos aportados, supuestos, estimaciones y resultados observados.

Las cifras, estudios, precios y resultados mencionados en cualquier contexto externo necesitan verificación antes de utilizarse en una propuesta real.

## Licencia

Este repositorio todavía no incluye una licencia de reutilización. Su publicación permite inspeccionarlo, pero no concede automáticamente permisos amplios para copiar, modificar o redistribuir el contenido.
