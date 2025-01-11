# Módulo 2: Fundamentos de la Automatización de Pruebas

## 1. ¿Qué es la Automatización de Pruebas?
- **Definición**: Proceso de ejecutar casos de prueba de forma automática utilizando scripts y herramientas especializadas.  
- **Beneficios**:  
  1. **Eficiencia** en la ejecución de pruebas repetitivas.  
  2. **Rapidez** en la detección de defectos (reducción del tiempo de regresión).  
  3. **Mayor cobertura** de pruebas con menos esfuerzo manual.  
- **Desafíos**:  
  1. **Mantenimiento** de los scripts y datos de prueba a medida que evoluciona el software.  
  2. **Coste inicial** en tiempo y recursos (selección de herramientas, capacitación, diseño de framework).  
  3. **Falsos positivos/negativos** si no se diseñan adecuadamente los casos y validaciones.  
- **Cuándo automatizar**:  
  - Casos de prueba **repetitivos** o que requieren gran cantidad de **datos**.  
  - Pruebas de **regresión** frecuentes.  
  - Escenarios críticos que deben ser verificados continuamente.  
- **Cuándo no automatizar**:  
  - Pruebas **exploratorias** o basadas en la experiencia intuitiva del tester.  
  - Casos **únicos** o **raramente** ejecutados.  
  - Validaciones que requieran **criterios subjetivos** (usabilidad, look & feel).

---

## 2. Frameworks de Automatización

### 2.1. Framework Lineal
- **Concepto**: Los casos de prueba se ejecutan de forma secuencial, tipo script paso a paso.  
- **Ventajas**:  
  - Sencillo de implementar.  
  - Ideal para proyectos pequeños o en etapas iniciales.  
- **Desventajas**:  
  - Difícil de mantener cuando el proyecto crece (alta duplicación de código).  

### 2.2. Framework Modular
- **Concepto**: Se divide la aplicación en módulos y se crea un script específico para cada uno.  
- **Ventajas**:  
  - Facilita el **mantenimiento** (si un módulo cambia, solo actualizas su script).  
  - **Reutilización de código** entre distintas suites de pruebas.  
- **Desventajas**:  
  - Requiere una **planificación inicial** sólida para la correcta modularización.  

### 2.3. Framework Basado en Datos (Data-Driven)
- **Concepto**: Se separan los datos de prueba de la lógica de los scripts, generalmente usando ficheros Excel, CSV o bases de datos.  
- **Ventajas**:  
  - Permite **ejecutar** el mismo script con múltiples conjuntos de datos de forma sencilla.  
  - **Facilita cambios** en los datos sin modificar la lógica del test.  
- **Desventajas**:  
  - Puede **complejizar** la estructura de los scripts y la configuración inicial.  

### 2.4. Framework Basado en Palabras Clave (Keyword-Driven)
- **Concepto**: Cada acción (keyword) se define de manera abstracta y se invoca desde tablas o ficheros externos (p. ej., "Abrir Navegador", "Ingresar Usuario").  
- **Ventajas**:  
  - **Separación clara** entre la lógica y la implementación.  
  - Usuarios no técnicos pueden definir pruebas usando palabras clave más simples.  
- **Desventajas**:  
  - Requiere un **esfuerzo inicial** considerable para definir y mantener las palabras clave.  
  - Mayor **complejidad** en la integración de pruebas muy específicas.

### 2.5. Framework Híbrido
- **Concepto**: Combina elementos de distintos tipos de frameworks (Data-Driven + Keyword-Driven, por ejemplo) para aprovechar lo mejor de cada enfoque.  
- **Ventajas**:  
  - **Flexibilidad** y escalabilidad en proyectos de mediana o gran envergadura.  
  - Permite manejar **escenarios complejos**.  
- **Desventajas**:  
  - Mayor **curva de aprendizaje** y de mantenimiento.  
  - Requiere una **arquitectura robusta** y personal con experiencia en distintos patrones.

---

## 3. Introducción a Herramientas de Automatización

### 3.1. Selenium WebDriver (Web)
- **Uso**: Automatización de aplicaciones web en navegadores (Chrome, Firefox, Edge).  
- **Características**:  
  - Biblioteca multiplataforma para **controlar** el navegador.  
  - Soporta **múltiples lenguajes** de programación (Java, Python, C#, JavaScript).  
  - Gran **comunidad** y **documentación**.  

### 3.2. Cypress (Web)
- **Uso**: Testing de aplicaciones web modernas, con gran foco en el ecosistema JavaScript.  
- **Características**:  
  - **Ejecución rápida** y en tiempo real dentro del navegador.  
  - Incluye un **dashboard** interactivo para depuración.  
  - **Ideal** para aplicaciones Single Page Application (React, Vue, Angular).

### 3.3. Playwright (Web)
- **Uso**: Marco de pruebas de Microsoft para aplicaciones web con un enfoque en la **automatización** de navegadores (Chromium, Firefox, WebKit).  
- **Características**:  
  - **Aislamiento** y **concurrencia** para pruebas rápidas.  
  - **Tests multiplataforma** (Windows, macOS, Linux).  
  - Soporta varios lenguajes: JavaScript/TypeScript, Python, C#, Java.

### 3.4. Appium (Móvil)
- **Uso**: Pruebas automatizadas de aplicaciones móviles (nativas, híbridas o web) en Android e iOS.  
- **Características**:  
  - Basado en el protocolo WebDriver.  
  - Admite **múltiples lenguajes** de programación (Java, Ruby, Python, JavaScript, etc.).  
  - Permite **pruebas cruzadas** en distintos dispositivos y versiones de SO.

### 3.5. [Opcional] Herramientas de Pruebas de API
- **RestAssured** (Java), **Postman** (colecciones y scripts), **Karate** (DSL)  
- **Uso**: Automatizar pruebas de **servicios web** (REST, SOAP).  
- **Características**:  
  - Ejecución de **requests** con **diferentes métodos** (GET, POST, PUT, DELETE).  
  - Validación de **respuestas** (estatus HTTP, cuerpo JSON/XML).  
  - Ideal para **microservicios** y escenarios donde la **API** es crucial.

---

## Conclusiones del Módulo 2
- **Automatizar** no es solo usar una herramienta, sino diseñar una **estrategia** que combine buenas prácticas, un **framework escalable** y la elección adecuada de **tecnologías**.  
- Conocer **cuándo** y **qué** automatizar evita invertir recursos en pruebas **innecesarias** o difíciles de mantener.  
- Existen diversos **frameworks** y **herramientas** para cubrir los distintos tipos de aplicaciones (web, móvil, APIs) y necesidades específicas de cada equipo.  
- Este módulo sienta las bases para que, en futuros módulos, se **profundice** en la implementación práctica de la automatización (Selenium, Appium, integraciones con CI/CD, etc.).