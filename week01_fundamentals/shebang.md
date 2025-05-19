# /usr/bin/env bash 

Es muy común y muy importante encontrar esta linea, le dice al sistema con qué programa debe ejecutar el script.

## 🧠 ¿Qué hace esta línea?
```bash
#!/usr/bin/env bash
```
### 🔍 Desglose:
* #! → Se llama shebang (hash + bang). Es una convención del sistema para indicar el intérprete del script.
*  /usr/bin/ven bash → Usa el comando env para encotar la ubicación de *bash* en el entorno del usuario (usr). 

##  ✅ ¿Por qué usar /usr/bin/env bash en vez de /bin/bash?

|Opción |Significado    |Portabilidad   |
|-------|---------------|---------------|
|#!/usr/bin/env bash| Usa directamente el bash que está en /bin/|❌ Puede fallar si bash no está ahí (por ejemplo, en macOS, BSD, etc.)|
|#!7usr/bin/env bash | Usa wl primer bash que encuentre en el PATH del usuario| ✅ Más portátil, más confiable en distintos entornos |

## 🧪 ¿Dónde lo verás?

* En la mayoría de scripts de proyectos, dotfiles, scripts de instalación, automatización, etc.

* Es una buena práctica adoptada por la mayoría de desarrolladores de Bash y otros lenguajes (#!/usr/bin/env python3, #!/usr/bin/env node, etc.).

## 🚀 Recomendación
Siempre que comiences un script de Bash, comienza con:
```bash
#!/usr/bin/env bash
```
Y asegurate de dar permisos de ejecución.
```bash
chmod +x your_scripy.sh
```