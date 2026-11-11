# Constitución — habits-cli
Principios innegociables. Toda spec, plan y tarea debe cumplirlos.

1. **Stack mínimo**: Python 3.12+ y solo biblioteca estándar; pytest es la
   única dependencia permitida, y solo para tests.
2. **La spec manda**: todo comportamiento se traza a un RF de la spec activa;
   sin RF no se implementa, y si falta una decisión se para y se pregunta.
3. **Núcleo puro**: `habits/core.py` no imprime, no lee consola ni toca
   archivos; la CLI solo parsea, llama al core y muestra el resultado.
4. **Tests como puerta**: cada RF tiene al menos un test; ninguna tarea se
   cierra sin `pytest -q` en verde.
5. **Un JSON local**: un único archivo JSON legible, sin BD ni red; su formato
   solo cambia si antes cambia la spec, y nunca se sobrescribe uno corrupto.
6. **Idioma**: código e identificadores en inglés; mensajes al usuario y
   documentación en español.
