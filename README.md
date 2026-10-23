# 🌸 Petal & Bloom — Boutique Floral & E-Commerce MVP

> Solución digital interactiva diseñada para la captación, personalización y cierre ágil de pedidos florales de temporada mediante arquitectura desacoplada de costo cero y liquidación directa.

[![Demo Live](https://img.shields.io/badge/Demo-Live_Online-2ea44f?style=for-the-badge&logo=github)](https://alan1721.github.io/demo-floreria/)
[![Stack](https://img.shields.io/badge/Frontend-React_18_•_Tailwind_CSS-1E3329?style=for-the-badge)](https://alan1721.github.io/demo-floreria/)
[![Deployment](https://img.shields.io/badge/Deploy-GitHub_Pages-blue?style=for-the-badge&logo=github)](https://alan1721.github.io/demo-floreria/)

---

## 📌 Diagnóstico y Propuesta de Valor

En el sector de la floristería de alta gama, las temporadas de alta demanda (San Valentín, Día de la Madre, festividades) generan cuellos de botella críticos en los canales de atención manual (WhatsApp/Instagram DMs). La atención individual para cotizar arreglos, coordinar dedicatorias y compartir datos bancarios resulta en:

* **Tasa de abandono elevada** debido a demoras en respuestas manuales.
* **Fricción operativa** al recopilar datos de despacho y dedicatorias de forma desordenada.
* **Costos fijos innecesarios** en infraestructura de servidores para negocios en etapa de validación.

**Petal & Bloom** solventa este problema actuando como un embudo digital automatizado: el cliente selecciona o arma su producto, define los parámetros logísticos y genera una orden estructurada con comprobante de pago en un solo flujo.

---

## ⚡ Arquitectura y Decisiones de Ingeniería

El proyecto se estructuró como una **Single Page Application (SPA)** de arquitectura desacoplada y ejecución en el lado del cliente (Client-Side Rendering):

* **Cero Costos de Mantenimiento:** Diseñado para ejecutarse íntegramente sobre infraestructura estática perimetral (CDN / GitHub Pages), reduciendo el costo recurrente de servidores a $0 USD/mes.
* **Orquestación Asíncrona sin Backend (Fase 1):** Codificación y empaquetado de payload transaccional en el cliente para el protocolo `wa.me`, asegurando una transición libre de intermediarios hacia el canal de atención comercial.
* **Gestión de Estado Reactivo:** Control de cesta de compras, personalización paramétrica de arreglos y cálculo de costos en tiempo de ejecución sin renderizados redundantes.

---

## 🛠️ Stack Tecnológico

| Capa | Tecnología | Justificación Técnica |
| :--- | :--- | :--- |
| **Core UI** | React 18 | Programación declarativa y gestión reactiva de estados modales y de carrito. |
| **Diseño y Estilos** | Tailwind CSS | Sistema de diseño botánico de alta fidelidad (`#1E3329`, `#E8B4B8`, `#FAF7F2`) con utilidades atómicas y carga perimetral. |
| **Iconografía** | Lucide Icons | Conjunto de glifos vectoriales ligeros optimizados para interfaces modernas. |
| **Pasarela Manual** | Web Clipboard API + WA URL Scheme | Copiado directo de credenciales bancarias y formateo estructurado URI-encoded. |
| **Alojamiento** | GitHub Pages / Cloudflare CDN | Distribución estática de alta disponibilidad con certificado SSL automático. |

---

## 📦 Módulos Funcionales
1. **Catálogo Segmentado:** Categorización dinámica (Romance, Cumpleaños, Aniversarios, Condolencias) con control de stock y etiquetas de temporada.
2. **Motor de Personalización ("Diseña tu Ramo"):** Sistema interactivo por pasos para configuración de flor principal, estilo de envoltura (papel coreano, kraft, malla) y complementos de lujo con balance de costos automático.
3. **Módulo de Logística y Tarjeta:** Restricción estricta de fechas pasadas para envíos, selección de franja diurna/vespertina y captura obligatoria de la dedicatoria.
4. **Checkout Transaccional con Copiado Rápido:** Despliegue de credenciales bancarias con feedback visual (`Copied!`) y exportación inmediata del pedido formalizado hacia WhatsApp.

---

## 🗺️ Roadmap de Implementación

### Fase 1: MVP Comercial & Validación (Estado Actual)
- [x] Interfaz de usuario responsive enfocada en dispositivos móviles (Mobile-First).
- [x] Catálogo digital con motor de armado personalizado.
- [x] Logística integrada en carrito y dedicatorias de tarjetas.
- [x] Módulo de transferencia bancaria con enlace asistido hacia WhatsApp.

### Fase 2: Automatización Transaccional & Pagos Digitales
- [ ] Implementación de pasarela de pagos con tarjeta de crédito/débito nacional e internacional.
- [ ] Orquestación de backend liviano para firma criptográfica de peticiones y prevención de fraude.
- [ ] Autenticación de usuarios mediante protocolo 3-D Secure (3DS2).
- [ ] Despliegue de Webhooks transaccionales para actualización automática del estado de las órdenes.

---

## 🚀 Despliegue y Ejecución Local

No requiere gestores de dependencias pesados (`npm`/`yarn`) para su previsualización:

```bash
# 1. Clonar el repositorio
git clone [https://github.com/Alan1721/demo-floreria.git](https://github.com/Alan1721/demo-floreria.git)

# 2. Navegar a la carpeta
cd demo-floreria

# 3. Ejecutar localmente
# Puedes abrir directamente el archivo index.html en cualquier navegador moderno
# o iniciar un servidor local rápido con Python:
python -m http.server 8000
