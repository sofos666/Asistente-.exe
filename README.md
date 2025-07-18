# Asistente Tanya

Este proyecto contiene un asistente virtual llamado Tanya, diseñado para automatizar el envío de mensajes de WhatsApp.

## Contenido del Repositorio

- `Asistente_tanya.exe`: El programa ejecutable para correr el asistente.
- `instrucciones_tanya.txt`: Archivo con las instrucciones de uso del asistente.
- `output.txt`: Archivo de salida generado por el asistente.
- `debug_paths.log`: Archivo de registro para depuración.

## Simulación de Comportamiento Humano

Para minimizar el riesgo de que WhatsApp detecte la automatización como un bot y potencialmente bloquee la cuenta, el script dentro del `.exe` incorpora técnicas que simulan la interacción humana:

- **Pausas Estratégicas**: Se utilizan pausas breves en momentos clave del proceso, como antes de escribir un mensaje o después de hacer clic en un botón. Esto imita el tiempo de reacción natural de una persona.

- **Escritura Gradual del Mensaje**: En lugar de pegar el mensaje completo de una sola vez, el script lo procesa línea por línea. Cada línea se escribe en el cuadro de texto y se simula la pulsación de `Shift + Enter` para crear un salto de línea, tal como lo haría un usuario. El mensaje final se envía con una pulsación de `Enter`.

- **Manejo de la Interfaz de Usuario**: El script espera activamente a que los elementos de la página (como el cuadro de texto o los botones) estén visibles y listos para interactuar antes de realizar cualquier acción. Esto evita errores y hace que la interacción sea más fluida y natural.

- **Perfil de Navegador Persistente**: La aplicación utiliza un perfil de Chrome dedicado. Esto permite que la sesión de WhatsApp Web se mantenga iniciada entre usos, evitando la necesidad de escanear el código QR repetidamente, que es un comportamiento normal del usuario.

Estas medidas, aunque no garantizan al 100% que la cuenta no sea marcada, reducen significativamente la probabilidad de detección al hacer que la automatización se parezca más al uso legítimo de la plataforma.