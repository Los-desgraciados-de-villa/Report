# Capítulo III: Requirements Specification

## 3.1 User Stories

Las user stories fueron elaboradas en sesiones de refinamiento con todo el equipo, basándonos en el análisis de las entrevistas y priorizadas mediante Pivotal Tracker.

| ID    | Título              | Descripción | Criterios de Aceptación |
|-------|---------------------|-------------|--------------------------|
| **US001** | Registro de usuario | Como propietario, quiero registrarme en la plataforma para poder generar certificados de mis inmuebles. | Dado que soy un nuevo usuario, cuando completo el formulario de registro correctamente, entonces recibo un email de confirmación y puedo acceder al sistema. |
| **US002** | Generar certificado | Como usuario registrado, quiero generar un certificado digital de mi inmueble para compartirlo con interesados. | Dado que he iniciado sesión, cuando completo la información requerida del inmueble, entonces el sistema genera un PDF certificado con sello digital. |
| **US003** | Verificar certificado | Como agente inmobiliario, quiero verificar la autenticidad de un certificado para validar la información del inmueble. | Dado que tengo un certificado digital, cuando ingreso el código de verificación, entonces el sistema confirma su autenticidad y muestra la información validada. |
| **US004** | Gestión de inmuebles | Como propietario, quiero gestionar mis inmuebles registrados para mantener actualizada su información. | Dado que he iniciado sesión, cuando accedo a mi panel de control, entonces puedo ver, editar y actualizar la información de mis inmuebles. |
