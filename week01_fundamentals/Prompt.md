# Prompt (\$\_)

El prompt (en español: indicador del sistema, invitación del sistema o simplemente prompt de la terminal) es el texto que aparece en la línea de comandos indicando que el sistema está listo para recibir una instrucción.

## 🖥️ ¿Qué es el prompt?


Es lo que ves cuando abres una terminal y el sistema espera que escribas algo. Ejemplo:
```bash
usuario@pc:~/Documentos$
```
Ahí es donde tú escribes comandos como `echo`, `ls`, `cd`, `etc`.

### 🔍 Componentes comunes del prompt
Un prompt típico en bash puede incluir:
```bash
usuario@hostname:directorio_actual$
```
Por ejemplo:
```bash
ana@debian:~/proyectos/bash-course$
```

|Parte |significado |
|------|------------|
| ana  | Nombre del usuar|
|@debian | Nombre del computador (hostname)|
|~/proyectos/... |Ruta del directorio actual|
| $ -  # |Simbolo de usuario normal, Simbolo del **ROOT**|

## ✏️ Personalizar el prompt

El prompt es definido por una variable llamada PS1.

Ejemplo básico:
```bash

PS1=">> "
```
Cambiará tu prompt a:
```ruby
>> _
```
🔧 Puedes editar tu prompt temporalmente o permanentemente modificando ~/.bashrc.

## 🧪 Ejemplo práctico

Para hacer que tu prompt muestre la hora actual:
```bash
PS1="[\t] \u@\h:\w\$ "
```
Donde:
|Código |Significado    |
|-------|---------------|
|\u     | Usuario       |
|\h  |Hostname|
|\w | Ruta actual|
|\t | Hora actual|
|\$ | $ o # segun si eres root o no |

Resultado:
```bash
[14:33:10] ana@debian:~/bash-course$
```

## ✅ ¿Por qué es importante?

* Te indica dónde estás (directorio).

* Muestra si eres usuario o root.

* Permite personalizar tu entorno para mayor productividad.