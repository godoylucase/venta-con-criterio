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

## Instalación compartida para Codex y Claude

Podés mantener una sola copia y enlazarla desde ambos clientes:

```bash
git clone https://github.com/godoylucase/venta-con-criterio.git ~/.agents/skills/venta-con-criterio
mkdir -p ~/.codex/skills ~/.claude/skills
ln -s ../../.agents/skills/venta-con-criterio ~/.codex/skills/venta-con-criterio
ln -s ../../.agents/skills/venta-con-criterio ~/.claude/skills/venta-con-criterio
```

Reiniciá el cliente o comenzá una sesión nueva después de instalarla.

La skill puede seleccionarse automáticamente cuando el pedido coincide con su descripción o invocarse explícitamente como `$venta-con-criterio` en clientes que admitan esa sintaxis.

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
