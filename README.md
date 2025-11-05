# Proyecto Automatización E2E + API Integrada

## Descripción del proyecto
Este proyecto valida los flujos de la aplicación **SauceDemo** y la API simulada **DummyJSON** mediante pruebas automatizadas:

- **API Tests:** implementados con **Karate**, para validar endpoints de autenticación y listado de usuarios.
- **E2E Tests:** implementados con **Cucumber + Playwright**, para validar login, flujo de compra y cierre de sesión.

El objetivo es garantizar que tanto la API como la interfaz web funcionen correctamente según los escenarios definidos.

---

## Requisitos previos
Para ejecutar este proyecto se requiere:

- Node.js >= 24
- npm
- Java 8 o superior (para ejecutar Karate)
- Git
- Navegador Chromium (Playwright lo instala automáticamente)

---

## Instalación del proyecto

1. Clonar el repositorio:

```bash
git clone https://github.com/tu-usuario/AutomatizacionE2E_ApiIntegradaCICD.git
cd AutomatizacionE2E_ApiIntegradaCICD

Instalar dependencias de Node.js:
npm ci

Instalar navegadores para Playwright:
npx playwright install --with-deps

Verificar instalación de Java para Karate:
java -version

Scripts disponibles

Ejecutar todos los tests (API + E2E):
npm run test:all

Solo tests E2E (Playwright + Cucumber):
npm run test:e2e

Solo tests API (Karate):
npm run test:api

Los comandos anteriores instancian los tests automáticamente, sin necesidad de configuraciones adicionales.

Estructura del proyecto
bash
Copiar código
src/
  api-tests/          # Pruebas API (Karate)
    login/
    products/
  e2e-tests/          # Pruebas E2E (Cucumber + Playwright)
    features/
    steps/
    support/
tools/
  karate.jar           # Ejecutable de Karate
package.json


Karate Reports: se generan en target/karate-reports

Playwright Reports: se generan en playwright-report

Ambos reportes pueden abrirse en cualquier navegador para revisar los resultados y los logs de ejecución.

Para descargar karate: https://github.com/karatelabs/karate/releases