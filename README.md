# InteligenciaArtificialUNAM20271
Repositorio de las actividades de IA en el semestre 271 UNAM
Notas:
# DEV, STAGE, PROD y requirements.txt

## DEV

DEV significa desarrollo.

Es el entorno donde se escribe, modifica y prueba el código mientras todavía está en construcción.

Características:

- El código cambia constantemente.
- Se hacen pruebas rápidas.
- Se pueden instalar nuevas librerías.
- Los errores no afectan a usuarios reales.

Crear entorno DEV:

```bash
python3 -m venv venv_dev
```

Activarlo en Mac:

```bash
source venv_dev/bin/activate
```

Salir del entorno:

```bash
deactivate
```

---

## STAGE

STAGE significa pruebas o preproducción.

Es un entorno parecido a producción donde se verifica que el programa funcione correctamente antes de publicarlo.

Características:

- Se hacen pruebas finales.
- Se busca detectar errores antes de PROD.
- Debe parecerse lo más posible al entorno real.

Crear entorno STAGE:

```bash
python3 -m venv venv_stage
```

Activarlo:

```bash
source venv_stage/bin/activate
```

Salir:

```bash
deactivate
```

---

## PROD

PROD significa producción.

Es el entorno final donde funciona el sistema real y donde pueden existir usuarios reales.

Características:

- El código debe estar probado.
- No se recomienda experimentar directamente aquí.
- Un error puede afectar el funcionamiento del sistema o a los usuarios.

Crear entorno PROD:

```bash
python3 -m venv venv_prod
```

Activarlo:

```bash
source venv_prod/bin/activate
```

Salir:

```bash
deactivate
```

---

## Flujo general

```text
DEV -> STAGE -> PROD
```

Significado:

```text
DEV   = desarrollar
STAGE = probar
PROD  = ejecutar el sistema final
```

Primero se desarrolla y modifica el código en DEV.

Luego se prueba en STAGE.

Finalmente, cuando todo funciona correctamente, se pasa a PROD.

---

## ¿Por qué no trabajar directamente en PROD?

No es recomendable porque PROD es el entorno donde funciona el sistema real.

Si se hacen cambios o entrenamientos directamente ahí, pueden ocurrir errores y afectar el funcionamiento del sistema.

Por eso se trabaja primero en DEV y STAGE antes de pasar a producción.

---

## requirements.txt

El archivo `requirements.txt` guarda las librerías necesarias para ejecutar el proyecto.

Ejemplo:

```text
numpy
pandas
streamlit
```

Para instalar todas las dependencias:

```bash
pip install -r requirements.txt
```

También se puede generar con:

```bash
pip freeze > requirements.txt
```

Esto guarda las librerías instaladas en el entorno.

---

## ¿Por qué es importante requirements.txt?

Permite que otra persona instale las mismas dependencias necesarias para ejecutar el proyecto.

También ayuda a reproducir el mismo entorno de trabajo.

Ejemplo:

```bash
pip install -r requirements.txt
```

---

## Relación con reproducibilidad

Usar entornos separados y controlar las dependencias permite repetir pruebas bajo condiciones similares.

Así, los resultados pueden volver a comprobarse y compararse con mayor facilidad.

---

## Comandos importantes para el examen

Crear:

```bash
python3 -m venv venv_dev
python3 -m venv venv_stage
python3 -m venv venv_prod
```

Activar DEV:

```bash
source venv_dev/bin/activate
```

Activar STAGE:

```bash
source venv_stage/bin/activate
```

Activar PROD:

```bash
source venv_prod/bin/activate
```

Salir:

```bash
deactivate
```

Instalar dependencias:

```bash
pip install -r requirements.txt
```

Guardar dependencias:

```bash
pip freeze > requirements.txt
```

---

## Resumen rápido

```text
DEV   -> Desarrollo
STAGE -> Pruebas / Preproducción
PROD  -> Producción

requirements.txt -> dependencias del proyecto
```

Frase clave:

```text
DEV desarrolla, STAGE prueba y PROD ejecuta.
```
