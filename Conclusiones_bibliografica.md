# Conclusiones y recomendaciones

## Conclusiones
Conclusiones Generales del Proyecto
Validación del Problema de Movilidad Urbana:

El análisis del problema de transporte en distritos de alto flujo (como San Isidro, Miraflores y Surco) confirmó la necesidad crítica de soluciones de micro-movilidad en el tramo de "última milla". La dependencia del transporte tradicional e informal genera congestión y altos costos para los usuarios, respaldando la propuesta de valor de biciGO como una alternativa rápida, económica y sostenible.

Diseño de Propuesta Centrado en el Usuario:

A través de herramientas metodológicas como la User Task Matrix, Journey Mapping y Empathy Mapping, se logró comprender a detalle el comportamiento de los perfiles B2C (usuarios frecuentes y transeúntes ocasionales). Esto permitió estructurar requisitos claros enfocados en la predictibilidad de tarifas, la facilidad de uso y la reducción de tiempos de espera.

Publicación Exitosa de la Landing Page:

Se logró desplegar e implementar la Landing Page oficial como primer entregable del proyecto. Esta plataforma estática/responsive cumple con comunicar de manera clara la propuesta de valor, el funcionamiento del servicio (Busca, Escanea, Muévete, Devuelve), las tarifas transparentes y el canal de contacto para la captación inicial de usuarios.

Retos y Desafíos en la Coordinación del Equipo:

Durante el desarrollo del proyecto se presentó cierta dificultad para coordinar los tiempos y sincronizar las entregas entre los integrantes del equipo. No obstante, mediante la organización del Sprint Backlog y el seguimiento del flujo de trabajo en Trello, se lograron redistribuir las actividades y canalizar los esfuerzos para cumplir con los entregables.

Avances y Adaptabilidad en el Frontend:

Se registraron avances significativos en la maquetación y estructura del frontend, aplicando de forma rigurosa el sistema de diseño (tokens de color #7BC617 y #263238, fuentes Poppins/Inter y principios de accesibilidad). La experiencia visual se adaptó de forma responsive para asegurar que tanto la versión móvil como la de escritorio mantengan coherencia visual y usabilidad.

Dificultad de Implementación y Fricción en el Flujo Principal de Bicicletas:

Se identificó una complejidad considerable al diseñar e implementar el flujo principal de alquiler y la interacción del usuario con las bicicletas (localización por GPS, escaneo QR del candado y finalización en BikePoints). Esta etapa genera fricción operativa debido a problemas potenciales como fallas de conexion con otras bounded context y por potenciales criticos a no ser lanzado el programa, se tuvo que suspeder ese apartado y por ello tambien la logica de bicigo.

## Recomendaciones
Conectar la aplicación web con el backend real:
El backend funciona correctamente en producción pero varias pantallas del frontend aún usan datos simulados. Se recomienda conectar ambas para que el usuario pueda alquilar una bicicleta, pagar y reportar incidencias de verdad.

Completar el inicio de sesión y la recuperación de cuenta:
El backend solo permite registrar usuarios y buscarlos por correo, sin recuperación de contraseña. Se recomienda terminar esta parte pues sirve para proteger los datos de las cuentas, como los pagos y/o viajes.

Corregir los problemas más graves de la evaluación heurística:
Se recomienda solucionar el botón "Generar datos aleatorios" involucrados al momento de insertar un método de pago, asi como la separación entre usuario y administrador en la gestión de bicicletas, el cambio seguro de contraseña y la mezcla de inglés y español puesto que son los que más afectan a la confianza del usuario así como el uso básico de la app.

Transparencia en los gastos de los planes:
El usuario no puede comparar objetivamente el Plan Tarifa con la Suscripción Pro porque no ve el precio por viaje. Se recomienda mostrar mensualmente cuánto ahorraría con el plan Pro de manera que sirva como ayuda al momento de decidir si vale la pena cambiar de plan.

Elegir un solo entorno de producción para cuidar la base de datos:
Hay una base de datos activa en Railway y otra detenida en Azure. Se recomienda quedarse con una y usar migraciones para cambiar tablas de manera que una modificación no ponga en riesgo los datos reales.

# Bibliografía

Comexperu (2024, 19 de abril) TRANSPORTE PÚBLICO EN LIMA EN RIESGO DE EMPEORAR (AUN) MÁS. ComexPeru. https://www.comexperu.org.pe/articulo/transporte-publico-en-lima-en-riesgo-de-empeorar-aun-mas

Grupo Banco Mundial (2024, 15 de octubre). Modernizar la gestión del tráfico en Lima con apoyo del Banco Mundial [Comunicado de prensa]. Banco Mundial. https://www.bancomundial.org/es/news/press-release/2024/10/15/modernizing-traffic-management-in-lima-with-world-bank-support

LimaComoVamos (2026, 16 de enero) Lima y Callao según sus habitantes (Reporte urbano de percepción ciudadana Edición 15). https://www.limacomovamos.org/wp-content/uploads/2026/01/EncuestaLCV2025.pdf

Ortega, R., Chavez, H. & Borja, M. (2026). Una ciudad desigual: ¿cómo afecta el tráfico la calidad de vida de los estudiantes?. Redacción Nexos. https://nexos.ulima.edu.pe/2026/03/05/una-ciudad-desigual-como-afecta-el-trafico-la-calidad-de-vida-de-los-estudiantes/

# Anexos
En esta sección se presentan los enlaces a los recursos de diseño, presentaciones de equipo y entornos desplegados para el proyecto:
