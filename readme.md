## Índice

0. [Ficha del proyecto](#0-ficha-del-proyecto)
1. [Descripción general del producto](#1-descripción-general-del-producto)
2. [Arquitectura del sistema](#2-arquitectura-del-sistema)
3. [Modelo de datos](#3-modelo-de-datos)
4. [Especificación de la API](#4-especificación-de-la-api)
5. [Historias de usuario](#5-historias-de-usuario)
6. [Tickets de trabajo](#6-tickets-de-trabajo)
7. [Pull requests](#7-pull-requests)

---

## 0. Ficha del proyecto

### \*\*0.1. Tu nombre completo:\*\* Francisco Eduardo Figueroa Mendoza

### \*\*0.2. Nombre del proyecto:\*\* The Secret Cap's Society

### \*\*0.3. Descripción breve del proyecto:\*\*

The Secret Caps Society es una plataforma exclusiva para revendedores de gorras New Era, donde cada tienda puede registrarse y publicar sus productos de manera gratuita. Más que un marketplace, es una comunidad secreta para verdaderos coleccionistas y fanáticos, diseñada para conectar a los amantes de las caps con las piezas más buscadas del mercado.

Con un modelo innovador, la sociedad permite a los vendedores crecer sin costos iniciales, mientras que los compradores acceden a una selección única de gorras difíciles de encontrar. Nuestro objetivo es impulsar a los resellers y ofrecer a los fans un espacio confiable, seguro y auténtico para conseguir sus caps favoritas.

### **0.4. URL del proyecto:**

> Puede ser pública o privada, en cuyo caso deberás compartir los accesos de manera segura. Puedes enviarlos a [alvaro@lidr.co](mailto:alvaro@lidr.co) usando algún servicio como [onetimesecret](https://onetimesecret.com/).

### 0.5. URL o archivo comprimido del repositorio

https://github.com/Intense-Development/the-secret-caps-society

---

## 1. Descripción general del producto

> Describe en detalle los siguientes aspectos del producto:

### **1.1. Objetivo:**

Qué valor aporta

- Crea un espacio exclusivo y confiable donde revendedores de gorras New Era pueden exhibir y vender sus productos sin costo de publicación.
- Facilita a los fanáticos el acceso a gorras auténticas, ediciones limitadas y modelos difíciles de conseguir en tiendas convencionales.
- Fomenta una comunidad alrededor de la pasión por las caps, conectando compradores y vendedores en un entorno seguro y especializado.

Qué soluciona

- La dispersión del mercado: actualmente los revendedores dependen de redes sociales o marketplaces generales, donde la visibilidad es baja y la confianza limitada.
- El problema de confianza: muchos compradores dudan de la autenticidad o calidad de los productos en otros canales.
- La falta de centralización: no existe un punto de encuentro único y especializado para caps lovers y resellers.

Para quién

- Resellers de gorras New Era: les da un canal dedicado, gratuito al inicio y con visibilidad segmentada hacia su público ideal.
- Fans y coleccionistas de caps: les ofrece un marketplace confiable para encontrar las piezas más exclusivas y validar su autenticidad.
- La comunidad cap culture: un espacio donde la moda urbana, la colección y la identidad se mezclan bajo una misma plataforma.

### **1.2. Características y funcionalidades principales:**

Para los revendedores de caps

1. Registro y perfil de tienda

- Cada reseller puede crear un perfil propio con logo, descripción y datos de contacto.
- Genera credibilidad y visibilidad frente a los compradores.

2. Publicación gratuita de productos

- Subida de gorras con fotos, descripción, precio, tallas y disponibilidad.
- Sin costo de publicación, lo que elimina barreras de entrada para pequeños revendedores.

3. Gestión de inventario

- Panel para editar, activar o desactivar productos según disponibilidad.
- Organización de catálogos con filtros (equipo, color, edición limitada, etc.).

4. Sistema de reputación

- Calificaciones y reseñas de compradores que refuerzan la confianza y autenticidad.

Para los compradores/coleccionistas 5. Marketplace especializado

- Búsqueda centralizada con filtros (equipo MLB/NFL/NBA, color, edición, talla).
- Experiencia enfocada 100% en caps, sin ruido de otros productos.

6. Validación de autenticidad

- Etiquetas o “badges” para vendedores verificados.
- Contenido educativo sobre cómo identificar caps originales.

7. Wishlist y alertas personalizadas

- Guardar modelos favoritos.
- Notificaciones cuando aparezca stock o un precio más bajo.

Para la comunidad y confianza 8. Chat seguro comprador-vendedor

- Comunicación dentro de la plataforma, sin exponer datos personales.
- Posibilidad de acordar entregas o resolver dudas antes de comprar.

9. Pagos protegidos (a futuro)

- Integración de pasarela de pago con sistema de escrow (el dinero se libera al confirmar recepción del producto).
- Reduce riesgos de fraude.

10. Contenido y cultura cap lover

- Blog y sección de noticias con lanzamientos, colaboraciones y tendencias.
- Genera comunidad más allá de la compraventa.

Para la plataforma y modelo de negocio

11. Comisiones por venta realizada

- Sin costo de entrada, pero se cobra un % al concretar la venta.
- Modelo escalable y justo: solo gana la plataforma si gana el vendedor.

12. Panel de estadísticas

- Métricas de ventas, visitas a productos, tendencias de búsqueda.
- Información valiosa para mejorar decisiones de stock y pricing.

### **1.3. Diseño y experiencia de usuario:**

![Homepage](screenshoots/homepage.png)
![Register](screenshoots/register/register-account-type.png)
![Register As Buyer](screenshoots/register/buyer/register-as-buyer-step-1.png)
![Register As Seller](screenshoots/register/seller/register-as-seller-step-1.png)
![Register As Seller](screenshoots/register/seller/register-as-seller-step-2.png)
![Register As Seller](screenshoots/register/seller/register-as-seller-step-3.png)
![Register As Seller](screenshoots/register/seller/register-as-seller-step-4.png)
![Register As Seller](screenshoots/register/seller/register-as-seller-successfully.png)
![Products](screenshoots/products/products.png)
![Product Detail](screenshoots/products/product-detail.png)
![Stores](screenshoots/stores/stores.png)
![Cart](screenshoots/cart/cart.png)
![404](screenshoots/404.png)

### **1.4. Instrucciones de instalación:**

1. Install dependencies

```bash
npm install
```

2. Configure environment variables

- Create a `.env.local` in the project root with:

```
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
```

3. Run the dev server

```bash
npm run dev
```

Open http://localhost:3000

## Testing (TDD)

- Unit/Component tests (Jest + RTL):

```bash
npm test
```

- Watch mode:

```bash
npm run test:watch
```

- CI mode:

```bash
npm run test:ci
```

MSW is pre-configured in `jest.setup.ts` with example handler `src/test/msw/handlers.ts`.

## E2E Tests (Playwright)

1. Install browsers (one-time):

```bash
npx playwright install
```

2. Run tests:

```bash
npm run e2e
```

Headed/UI modes are available via `e2e:headed` and `e2e:ui`.

## 2. Arquitectura del Sistema

### **2.1. Diagrama de arquitectura:**

> Usa el formato que consideres más adecuado para representar los componentes principales de la aplicación y las tecnologías utilizadas. Explica si sigue algún patrón predefinido, justifica por qué se ha elegido esta arquitectura, y destaca los beneficios principales que aportan al proyecto y justifican su uso, así como sacrificios o déficits que implica.

### **2.2. Descripción de componentes principales:**

> Describe los componentes más importantes, incluyendo la tecnología utilizada

### **2.3. Descripción de alto nivel del proyecto y estructura de ficheros**

> Representa la estructura del proyecto y explica brevemente el propósito de las carpetas principales, así como si obedece a algún patrón o arquitectura específica.

### **2.4. Infraestructura y despliegue**

> Detalla la infraestructura del proyecto, incluyendo un diagrama en el formato que creas conveniente, y explica el proceso de despliegue que se sigue

### **2.5. Seguridad**

> Enumera y describe las prácticas de seguridad principales que se han implementado en el proyecto, añadiendo ejemplos si procede

### **2.6. Tests**

> Describe brevemente algunos de los tests realizados

---

## 3. Modelo de Datos

### **3.1. Diagrama del modelo de datos:**

> Recomendamos usar mermaid para el modelo de datos, y utilizar todos los parámetros que permite la sintaxis para dar el máximo detalle, por ejemplo las claves primarias y foráneas.

### **3.2. Descripción de entidades principales:**

> Recuerda incluir el máximo detalle de cada entidad, como el nombre y tipo de cada atributo, descripción breve si procede, claves primarias y foráneas, relaciones y tipo de relación, restricciones (unique, not null…), etc.

---

## 4. Especificación de la API

> Si tu backend se comunica a través de API, describe los endpoints principales (máximo 3) en formato OpenAPI. Opcionalmente puedes añadir un ejemplo de petición y de respuesta para mayor claridad

---

## 5. Historias de Usuario

> Documenta 3 de las historias de usuario principales utilizadas durante el desarrollo, teniendo en cuenta las buenas prácticas de producto al respecto.

**Historia de Usuario 1**

**Historia de Usuario 2**

**Historia de Usuario 3**

---

## 6. Tickets de Trabajo

> Documenta 3 de los tickets de trabajo principales del desarrollo, uno de backend, uno de frontend, y uno de bases de datos. Da todo el detalle requerido para desarrollar la tarea de inicio a fin teniendo en cuenta las buenas prácticas al respecto.

**Ticket 1**

**Ticket 2**

**Ticket 3**

---

## 7. Pull Requests

> Documenta 3 de las Pull Requests realizadas durante la ejecución del proyecto

**Pull Request 1**

**Pull Request 2**

**Pull Request 3**
