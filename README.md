<p align="center">
  <img src="assets/akame-banner.png" alt="Akame Plugins" width="720">
</p>

# AkameCooldowns

Bloqueos y cooldowns de items para servidores **Paper 1.21**, globales o por región de **WorldGuard**. Autor: **Motlys**.

> El código fuente de este plugin es privado. Este repositorio es solo una presentación del proyecto.

Un bloqueo es un bloqueo de verdad: un escudo bloqueado no se puede levantar, una lanza bloqueada no ataca ni se carga, y una perla bloqueada no teletransporta aunque se lance desde fuera de la región.

## Características

- **Bloqueos y cooldowns** para cualquier item, también armas, comida, bloques y proyectiles, en todo el servidor o solo en regiones.
- **Grupos de items** como `@spears`, `@swords`, `@maces`, `@shields` o `@wind-charges`, que cubren todas las variantes de la versión del servidor. Se pueden crear grupos propios, incluso anidados.
- **Regiones con prioridad:** manda la región de mayor prioridad que tenga una regla sobre el item. Una región puede permitir lo que está bloqueado en todo el servidor.
- **Proyectiles bien tratados:** una perla o una carga de viento lanzada desde fuera de una región bloqueada no teletransporta ni empuja a nadie dentro, y se devuelve al jugador.
- **WorldGuard opcional:** sin él funcionan las reglas globales.
- **Paper Plugin** con `paper-plugin.yml`, visible en el apartado "Paper Plugins".
- **Configuración clara:** `config.yml`, `rules.yml` y `messages.yml`, con duraciones como `1m30s`. Si un archivo tiene un error, se indica el archivo y la línea, y se conserva la configuración anterior.
- **Comandos que respetan tus comentarios:** editan `rules.yml` sin perder lo que escribiste.
- **Migración automática** de las reglas y opciones de ItemCooldownPlus la primera vez.
- **Avisos configurables:** action bar, sonido, barra de jefe y cooldown visual de Minecraft.

## Comandos

Alias: `/acd` y `/cdp`.

| Comando | Permiso | Descripción |
|---|---|---|
| `/acd block <add\|remove> <región\|global> <item\|@grupo>` | `akamecooldowns.admin` | Bloquear o desbloquear |
| `/acd allow <add\|remove> <región> <item\|@grupo>` | `akamecooldowns.admin` | Permitir en una región lo bloqueado globalmente |
| `/acd cooldown set\|remove ...` | `akamecooldowns.admin` | Poner o quitar un cooldown |
| `/acd list` / `clear` / `reset` / `reload` | `akamecooldowns.admin` | Ver, borrar, reiniciar y recargar |
| `/acd check` / `groups` | `akamecooldowns.check` | Qué reglas afectan al item de tu mano y qué grupos hay |

`akamecooldowns.bypass` ignora todos los bloqueos y cooldowns.

## Requisitos

- Paper 1.21.x con Java 21 o superior.
- Opcional: WorldGuard 7.x.
- No es compatible con Folia.

## Pruebas

Probado con pruebas unitarias y en un servidor Paper 1.21.11 real con WorldGuard, con jugadores simulados. No se ha probado en Paper 26.x. Los cooldowns se guardan en memoria: sobreviven a que un jugador se desconecte, pero no a reiniciar el servidor.

---

<sub>Parte de **[Akame Plugins](https://github.com/AkamePlugins)**.</sub>
