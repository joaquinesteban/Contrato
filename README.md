# Contrato Freelance — Firma Digital

Contrato de prestación de servicios (desarrollo web / automatizaciones) con firma digital integrada. Pensado para freelancers que necesitan enviar un acuerdo a cada cliente nuevo y que ambas partes lo firmen desde el navegador.

## ¿Qué hace?

- Contrato editable con los datos de cada proyecto (cliente, freelancer, monto, fechas, alcance).
- Cláusulas base: objeto del acuerdo, servicios, entregables, honorarios, revisiones, propiedad intelectual, confidencialidad y cancelación.
- Dos paneles de firma (freelancer y cliente) donde se dibuja con mouse o dedo.
- Botón **Descargar PDF**: genera el contrato completo en PDF, con las firmas incluidas, respetando los cortes de página por cláusula (no corta texto ni firmas a la mitad) y en alta calidad (PNG sin pérdida).

## Estructura del repo

```
Contrato_Freelance.html   → la página del contrato, un solo archivo (HTML/CSS/JS)
```

## Uso

Subí `Contrato_Freelance.html` a Vercel, Netlify o cualquier hosting estático (renombrado como `index.html` en la raíz). Es un archivo único, sin build ni dependencias que instalar.

## Flujo con el cliente

1. Completás los datos del proyecto (cliente, monto, fechas) y le mandás el link.
2. Vos firmás primero en tu panel ("Freelancer"), así el PDF que descargue el cliente ya sale con ambas firmas.
3. El cliente entra, revisa el contrato, firma en su panel y toca **Descargar PDF**.
4. Te reenvía el PDF firmado por mail (o el medio que uses para coordinar).

## Stack

HTML / CSS / JavaScript vanilla. Sin frameworks ni build step.

- [html2canvas](https://github.com/niklasvh/html2canvas) — captura cada sección del contrato como imagen para el PDF.
- [jsPDF](https://github.com/parallax/jsPDF) — arma el PDF final, bloque por bloque, respetando los saltos de página.

## Notas

- El contrato es una plantilla de partida, no asesoramiento legal. Para montos grandes o clientes corporativos, conviene que lo revise un abogado.
- Todo corre en el navegador del cliente: nada se envía a un servidor propio ni de terceros.
