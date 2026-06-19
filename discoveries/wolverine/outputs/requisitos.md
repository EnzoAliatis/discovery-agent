# Requisitos Candidatos — Wolverine

> Derivados exclusivamente de las entrevistas de `discoveries/wolverine/interviews/`.
> Sin invención: cada requisito cita la fuente que lo respalda.

---

## Requisitos funcionales

- **[R-01]** El sistema debe mostrar la disponibilidad real de espacios/horarios en tiempo real, unificando todos los canales de entrada en una sola vista.
  - Tipo: funcional
  - Origen: `dueno-bar.md` · Dueño de Bar ("Tener un solo lugar donde ver la disponibilidad real")

- **[R-02]** Los clientes deben poder realizar una reserva de forma autónoma, sin intermediación del dueño o del técnico.
  - Tipo: funcional
  - Origen: `dueno-bar.md` · Dueño de Bar ("Que la gente reserve sola"); `tecnico-piscinas.md` · Técnico Independiente ("Que los clientes vean mis horarios disponibles")

- **[R-03]** El sistema debe calcular automáticamente los horarios disponibles considerando la duración específica de cada tipo de servicio, bloqueando los intervalos ya comprometidos.
  - Tipo: funcional
  - Origen: `dueno-spa.md` · Dueña de Spa ("Que el sistema entienda cuánto dura cada servicio y solo muestre horarios realmente disponibles")

- **[R-04]** El sistema debe enviar recordatorios automáticos a los clientes antes de su cita o visita para reducir los no-shows.
  - Tipo: funcional
  - Origen: `dueno-spa.md` · Dueña de Spa ("me ayudaría mucho que enviara recordatorios porque hay clientes que simplemente no aparecen")

- **[R-05]** El sistema debe permitir gestionar cambios de último momento (cancelaciones y reagendamientos) desde una interfaz centralizada, recalculando la disponibilidad automáticamente.
  - Tipo: funcional
  - Origen: `tecnico-piscinas.md` · Técnico Independiente ("Un cliente cancela, otro quiere adelantar la visita… Termino moviendo todo manualmente")

- **[R-06]** El sistema debe bloquear automáticamente un horario o mesa en el momento en que se confirma una reserva, impidiendo que se acepte otra reserva sobre el mismo espacio/horario.
  - Tipo: funcional
  - Origen: `dueno-bar.md` · Dueño de Bar (dobles reservas); `dueno-spa.md` · Dueña de Spa ("acepto una reserva y después descubro que el horario ya estaba comprometido")

---

## Requisitos no funcionales

- **[R-07]** El sistema debe ser accesible desde dispositivos móviles, dado que los usuarios actuales operan principalmente desde el teléfono (WhatsApp, calendario del celular).
  - Tipo: no funcional — accesibilidad / portabilidad
  - Origen: `dueno-bar.md` · Dueño de Bar (menciona WhatsApp); `tecnico-piscinas.md` · Técnico Independiente ("calendario del celular")

- **[R-08]** El sistema no debe requerir conocimientos técnicos avanzados para su operación diaria: los tres perfiles entrevistados gestionan sus negocios sin herramientas digitales especializadas.
  - Tipo: no funcional — usabilidad
  - Origen: `dueno-bar.md`, `dueno-spa.md`, `tecnico-piscinas.md` (los tres usan soluciones informales como WhatsApp y agendas en papel/celular)
