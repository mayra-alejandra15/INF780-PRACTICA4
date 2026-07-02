# Práctica 4 - Pruebas de Rendimiento con Apache JMeter

## Descripción

Este proyecto corresponde a la Práctica 4 de la materia INF780 - Verificación y Validación de Software. Se realizaron pruebas de rendimiento sobre la API MoviesAPI utilizando Apache JMeter para evaluar su comportamiento bajo diferentes niveles de carga.

Las pruebas implementadas fueron:

- Smoke Test (Prueba de humo)
- Load Test (Prueba de carga)
- Stress Test (Prueba de estrés)
- Spike Test (Prueba de picos)

Además, se generaron reportes HTML y archivos de resultados (.jtl) para el análisis de métricas.

---

# Tecnologías utilizadas

- Node.js
- NestJS
- PostgreSQL
- Apache JMeter 5.6.3
- Java 17
- Git
- GitHub

---

# Requisitos

Antes de ejecutar el proyecto debe tener instalado:

- Node.js
- PostgreSQL
- Java 17 o superior
- Apache JMeter 5.6.3

---

# Instalación

Instalar las dependencias del proyecto:

```bash
npm install
```

---

# Ejecución de la API

Iniciar el servidor de desarrollo:

```bash
npm run start:dev
```

La API estará disponible en:

```
http://localhost:3000
```

Puede comprobar su funcionamiento ingresando a:

```
http://localhost:3000/movies
```

---

# Planes de prueba

Los planes desarrollados en Apache JMeter son:

| Archivo | Descripción |
|----------|-------------|
| smoke.jmx | Verificación básica del funcionamiento de la API |
| carga.jmx | Prueba con múltiples usuarios concurrentes |
| estres.jmx | Incremento progresivo de usuarios hasta encontrar el límite del sistema |
| picos.jmx | Simulación de un incremento brusco de usuarios |

---

# Ejecución en modo gráfico (GUI)

Abrir Apache JMeter y ejecutar el archivo correspondiente:

- smoke.jmx
- carga.jmx
- estres.jmx
- picos.jmx

---

# Ejecución en modo no-GUI

## Smoke

```bash
jmeter -n -t smoke.jmx -l smoke.jtl -e -o ReporteSmoke
```

## Carga

```bash
jmeter -n -t carga.jmx -l carga.jtl -e -o ReporteCarga
```

## Estrés

```bash
jmeter -n -t estres.jmx -l estres.jtl -e -o ReporteEstres
```

## Picos

```bash
jmeter -n -t picos.jmx -l picos.jtl -e -o ReportePicos
```

---

# Resultados generados

La ejecución de las pruebas genera automáticamente:

- Archivos `.jtl`
- Dashboard HTML
- Aggregate Report
- Summary Report
- View Results Tree

Los reportes HTML se encuentran en las carpetas:

- ReporteSmoke
- ReporteCarga
- ReporteEstres
- ReportePicos

---

# Autor

**Mayra Alejandra Mamani Quispe** ,

**Anahi Gutierrez Cardenas**

Ingeniería Informática

Universidad Autónoma Tomás Frías (UATF)

Materia: INF780 - Verificación y Validación de Software    
