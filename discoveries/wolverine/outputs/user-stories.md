# User Stories — Wolverine

> Generadas desde `personas.md` y `requisitos.md` de `discoveries/wolverine/outputs/`.
> Toda historia cita la entrevista fuente que la respalda.

---

## Historias del MVP

### Núcleo de valor: agenda centralizada con reserva autónoma y bloqueo automático

Los dolores que más se repiten entre personas —dobles reservas (bar y spa) y tiempo
perdido en gestión manual (spa y técnico)— convergen en un mismo núcleo: un sistema
que centraliza la disponibilidad, deja que el cliente reserve solo y bloquea el
espacio en el acto.

---

- **[US-01]** Como dueño de negocio, quiero ver en tiempo real qué espacios o turnos
  están disponibles para gestionar mi agenda desde un solo lugar sin tener que revisar
  WhatsApp, Instagram o el calendario del celular.
  - **Criterios de aceptación:**
    - Dado que existen reservas confirmadas en el sistema, cuando el dueño abre la
      vista de disponibilidad, entonces ve los espacios ocupados y los libres
      actualizados al momento presente.
    - Dado que un cliente acaba de confirmar una reserva, cuando el dueño consulta la
      vista, entonces el nuevo espacio aparece bloqueado en menos de 5 segundos.
  - **Fuente:** `dueno-bar.md`, `tecnico-piscinas.md`

- **[US-02]** Como cliente, quiero poder reservar una mesa, cita o visita técnica
  directamente en el sistema para no tener que escribir por WhatsApp ni llamar.
  - **Criterios de aceptación:**
    - Dado que accedo a la vista de disponibilidad y elijo un espacio libre, cuando
      completo mis datos y confirmo, entonces recibo confirmación inmediata y el
      espacio queda bloqueado.
    - Dado que el espacio elegido fue tomado mientras llenaba el formulario, cuando
      intento confirmar, entonces el sistema me avisa que ya no está disponible y me
      muestra las alternativas libres.
  - **Fuente:** `dueno-bar.md`, `tecnico-piscinas.md`

- **[US-03]** Como dueña de spa, quiero configurar la duración de cada tipo de
  servicio para que el sistema solo muestre turnos donde el servicio completo cabe
  sin solaparse con la siguiente reserva.
  - **Criterios de aceptación:**
    - Dado que configuro un servicio de 90 minutos, cuando el sistema calcula
      disponibilidad, entonces no ofrece turnos donde quedan menos de 90 minutos
      antes de la siguiente reserva.
    - Dado que una cita de 60 minutos empieza a las 10:00, cuando un cliente intenta
      reservar a las 10:30, entonces el sistema rechaza la solicitud y muestra el
      próximo turno libre.
  - **Fuente:** `dueno-spa.md`

- **[US-04]** Como dueño de negocio, quiero que el sistema bloquee automáticamente
  el espacio o turno en el instante en que se confirma una reserva para que nunca
  ocurra una doble reserva.
  - **Criterios de aceptación:**
    - Dado que dos clientes intentan reservar el mismo espacio en paralelo, cuando
      ambos confirman, entonces solo uno recibe confirmación; el otro ve el espacio
      como no disponible.
    - Dado que una reserva se acaba de confirmar, cuando cualquier otro usuario
      intenta reservar el mismo espacio o turno, entonces el sistema lo muestra
      bloqueado de forma inmediata.
  - **Fuente:** `dueno-bar.md`, `dueno-spa.md`

---

## Historias fuera del MVP (segunda iteración)

Estas historias responden a dolores reales, pero no atacan la causa raíz de las
dobles reservas ni la adopción del canal nuevo. Entran en la segunda iteración,
una vez validado que los clientes usan el sistema para reservar.

- **[US-05]** Como dueña de spa, quiero que el sistema envíe recordatorios
  automáticos a los clientes antes de su cita para reducir los no-shows.
  - **Criterios de aceptación:**
    - Dado que una cita está confirmada, cuando faltan 24 horas, entonces el cliente
      recibe un recordatorio por el canal configurado (correo electrónico o SMS).
    - Dado que el cliente recibe el recordatorio, cuando confirma asistencia, entonces
      el sistema registra la confirmación y la cita permanece activa.
  - **Fuente:** `dueno-spa.md`
  - **Por qué fuera del MVP:** reduce el impacto del problema (tiempo muerto), pero
    no es la causa raíz. Primero validar adopción del canal de reserva.

- **[US-06]** Como técnico independiente o dueña de spa, quiero poder cancelar o
  reagendar una cita desde el sistema para que la disponibilidad se recalcule
  automáticamente sin tener que hacerlo a mano.
  - **Criterios de aceptación:**
    - Dado que un cliente cancela, cuando registro la cancelación en el sistema,
      entonces el espacio vuelve a aparecer disponible de forma inmediata.
    - Dado que reagendo una cita, cuando confirmo el nuevo horario, entonces el
      espacio anterior queda libre y el nuevo queda bloqueado en el acto.
  - **Fuente:** `tecnico-piscinas.md`, `dueno-spa.md`
  - **Por qué fuera del MVP:** complejiza el flujo de cambios antes de validar que
    los clientes adoptan el canal nuevo para reservas originales.

---

## Mapa de trazabilidad US → Requisito → Evidencia

| US | Requisito | Fuente(s) |
|---|---|---|
| US-01 | R-01 | `dueno-bar.md`, `tecnico-piscinas.md` |
| US-02 | R-02 | `dueno-bar.md`, `tecnico-piscinas.md` |
| US-03 | R-03 | `dueno-spa.md` |
| US-04 | R-06 | `dueno-bar.md`, `dueno-spa.md` |
| US-05 | R-04 | `dueno-spa.md` |
| US-06 | R-05 | `tecnico-piscinas.md`, `dueno-spa.md` |
