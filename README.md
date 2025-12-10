# ⚙️ README: Calculadora IEDMT (Impuesto de Matriculación)

## 🚀 Sobre la Aplicación

La **Calculadora IEDMT** es una herramienta ligera y esencial desarrollada para la gestoría, diseñada para **calcular de forma rápida y precisa el importe del Impuesto Especial sobre Determinados Medios de Transporte (IEDMT)**, basándose en la base imponible y el nivel de emisiones de CO2 (casilla V7) del vehículo.

**Objetivo principal:** Simplificar la liquidación del IEDMT para la matriculación de vehículos en Andalucía, integrando automáticamente los cambios históricos en el IVA y los tramos de emisiones vigentes.

## ✨ Características Clave

* **Cálculo Preciso:** Utiliza la fórmula ajustada para determinar el importe del IEDMT.
* **Lógica Histórica del IVA:** Determina automáticamente el IVA aplicable (16%, 18% o 21%) según la fecha oficial de la primera matriculación (BOE), esencial para la correcta valoración.
    * *Fechas de corte:* 1 de Julio de 2010 y 1 de Septiembre de 2012.
* **Tramos de Emisiones (V7):** Aplica el tipo impositivo correcto (0%, 4.75%, 9.75% o 14.75%) según el rango de CO2.
* **Portabilidad Total:** Implementada en un único archivo HTML/JavaScript, funciona **localmente** en cualquier navegador de la red, sin necesidad de conexión a Internet ni instalaciones.

## 🛠️ Uso e Instalación

1.  **Descarga:** Guarda el archivo `Calculadora.html` en una carpeta de tu ordenador o en la carpeta compartida de la red local de la gestoría.
2.  **Ejecución:** Simplemente haz doble clic en el archivo `Calculadora.html`. Se abrirá automáticamente en tu navegador predeterminado (Chrome, Edge, Firefox, etc.).
3.  **Documentación:** Dentro de la aplicación, haz clic en **"Mostrar/Ocultar Ayuda y Base Imponible"** para acceder a la guía detallada sobre cómo obtener la Base Imponible a través del portal de la Junta de Andalucía (ATRIAN).

## 📝 Fórmula Empleada

El cálculo se realiza internamente aplicando la siguiente fórmula, donde la Base Imponible incluye el IVA según su fecha de origen:

$$\text{IEDMT a Pagar} = \left( \frac{\text{Base Imponible}}{1 + \text{IVA} + \text{V7}} \right) \times \text{V7}$$

Donde:
* **BI:** Base Imponible (Valor residual Junta de Andalucía).
* **IVA:** Tipo de IVA histórico (0.16, 0.18 o 0.21).
* **V7:** Tipo impositivo por emisiones de CO2 (0.00 a 0.1475).

***
