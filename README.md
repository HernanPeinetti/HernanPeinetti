<div align="center">

# Hernán Peinetti

### Data Engineer Jr. · Python · SQL · Airflow

**Armo pipelines de datos reproducibles: ingesta, validación, modelado y orquestación.**
Vengo del desarrollo web y me especialicé en datos. Busco mi primer rol en un equipo de datos.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/TU-USUARIO/)
[![Email](https://img.shields.io/badge/Escribime-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:TU-EMAIL)
[![CV](https://img.shields.io/badge/Ver_CV-2ea043?style=for-the-badge&logo=readdotcv&logoColor=white)](TU-LINK-AL-CV)

📍 Argentina · 🟢 Disponible · 🌎 Remoto o híbrido · 🗣️ Español · Inglés TU-NIVEL

</div>

---

## 👋 Sobre mí

Trabajé como desarrollador web y en ese camino descubrí que lo que más me interesaba era la parte de atrás: de dónde vienen los datos, cómo se mueven entre sistemas y por qué a veces no se puede confiar en ellos. Así que me formé en ingeniería de datos y hoy construyo pipelines completos.

Estoy arrancando en el rubro, y eso significa dos cosas: todavía tengo mucho por aprender, y aprendo rápido porque estoy metido en esto todos los días. Lo que sí traigo es la costumbre de escribir código ordenado, documentar lo que hago y trabajar con Git como corresponde.

**Lo que busco:** un equipo donde pueda sumar desde el primer día en tareas de ingesta, transformación y calidad de datos, y donde haya gente con más experiencia de la que aprender.

---

## 🎯 Proyecto principal

<div align="center">

### [Pipeline de datos end-to-end →](https://github.com/HernanPeinetti/NOMBRE-DEL-REPO)

*De una API pública a tablas listas para analizar, orquestado y testeado.*

<!-- Cuando lo tengas corriendo, grabá un GIF del DAG en Airflow y descomentá esto.
     Es lo que más impacto genera en un recruiter técnico.
<img src="docs/pipeline.gif" width="760" alt="DAG de Airflow ejecutándose">
-->

</div>

```mermaid
flowchart LR
    A("🌐 API pública"):::source --> B("⚙️ Airflow<br/><b>extract</b>"):::orch
    B --> C[("🐘 PostgreSQL<br/><b>raw</b>")]:::store
    C --> D("🔧 dbt<br/><b>staging</b>"):::transform
    D --> E("📦 dbt<br/><b>marts</b>"):::transform
    E --> F("📊 Consultas / Dashboard"):::output
    Q{{"✅ Tests de calidad"}}:::quality -.-> C
    Q -.-> E

    classDef source fill:#1f6feb,stroke:#58a6ff,stroke-width:2px,color:#fff
    classDef orch fill:#017CEE,stroke:#58a6ff,stroke-width:2px,color:#fff
    classDef store fill:#4169E1,stroke:#8b9dff,stroke-width:2px,color:#fff
    classDef transform fill:#FF694B,stroke:#ff9b85,stroke-width:2px,color:#fff
    classDef output fill:#2ea043,stroke:#56d364,stroke-width:2px,color:#fff
    classDef quality fill:#8957e5,stroke:#bc8cff,stroke-width:2px,color:#fff
```

**Qué hace cada pieza**

| Etapa | Qué resuelve |
|---|---|
| **Extracción** | Un DAG de Airflow consulta la API todos los días, con reintentos ante fallas de red |
| **Capa raw** | Guarda el dato tal cual llegó, sin transformar, para poder reprocesar si algo sale mal |
| **Transformación** | Modelos dbt en dos capas: staging limpia y tipa, marts arma las tablas de negocio |
| **Calidad** | Tests que frenan la publicación si aparecen nulos, duplicados o valores fuera de rango |
| **Infraestructura** | Todo levanta con `docker compose up`, para que cualquiera lo pueda correr |

**Qué aprendí construyéndolo**

- Por qué un pipeline tiene que ser **idempotente**: la primera versión duplicaba filas al re-ejecutarla, y lo resolví con carga por clave natural
- Que **guardar el dato crudo** te salva: cuando cambié el modelado, pude reprocesar todo sin volver a pegarle a la API
- Que los tests de datos atrapan errores que los tests de código no ven

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=for-the-badge&logo=apacheairflow&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=for-the-badge&logo=dbt&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

---

## 📦 Otros proyectos

<table>
<tr>
<td width="50%" valign="top">

### ⚙️ [ETL Pipeline](https://github.com/HernanPeinetti/etl-pipeline)

Extrae datos de un archivo o API, valida calidad y los carga en un esquema documentado.

**Lo interesante:** separa extracción, validación y carga en módulos testeables por separado.

`Python` `Pandas` `SQL` `PostgreSQL`

</td>
<td width="50%" valign="top">

### 🧪 [Data Quality Checks](https://github.com/HernanPeinetti/NOMBRE-DEL-REPO)

Suite reutilizable de validaciones: nulos, duplicados, rangos, formatos y frescura del dato.

**Lo interesante:** se configura por YAML, así que sirve para cualquier tabla sin tocar código.

`Python` `SQL` `pytest`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 📊 [Análisis de datos abiertos](https://github.com/HernanPeinetti/NOMBRE-DEL-REPO)

Ingesta de un dataset público, modelado en PostgreSQL y consultas que responden preguntas concretas.

**Lo interesante:** muestra el SQL, no solo el resultado. Ventanas, CTEs y agregaciones.

`SQL` `PostgreSQL` `Python`

</td>
<td width="50%" valign="top">

### 🐳 [Entorno reproducible](https://github.com/HernanPeinetti/docker-starter)

Plantilla con Docker Compose y GitHub Actions que uso como base para arrancar proyectos.

**Lo interesante:** tests y linter corriendo en CI desde el primer commit.

`Docker` `GitHub Actions` `Linux`

</td>
</tr>
</table>

---

## 🧰 Stack

<div align="center">

**Lenguajes y datos**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

**Orquestación y transformación**

![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white)

**Entorno de trabajo**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/CI-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

</div>

---

## 📐 Cómo trabajo

> **Idempotencia primero.** Un pipeline que se re-ejecuta no debería duplicar nada.
>
> **Validar antes de cargar.** Los datos malos se detectan en el pipeline, no en el dashboard.
>
> **Un comando para levantarlo.** Si otra persona no lo puede correr, no está terminado.
>
> **Documentar la decisión, no solo el código.** El README explica *por qué*, no solo *cómo*.
>
> **Preguntar temprano.** Prefiero consultar una duda hoy que rehacer el trabajo la semana que viene.

---

## 🌱 En qué estoy ahora

| Tema | Estado |
|---|---|
| Modelado dimensional (hechos y dimensiones) | 🟢 Aplicándolo en proyectos |
| Testing de datos con Great Expectations | 🟡 En curso |
| PySpark | 🟡 En curso |
| AWS (S3, Glue, Redshift) | 🔵 Siguiente en la lista |

<sub>Antes de datos trabajé como desarrollador web con JavaScript, Node.js, React y MySQL. De ahí traigo la base de SQL y la costumbre de trabajar en equipo con Git.</sub>

---

<div align="center">

### ¿Buscás a alguien junior con ganas para tu equipo de datos?

Estoy disponible y con muchas ganas de sumarme a un equipo donde pueda aportar y crecer.

[![Email](https://img.shields.io/badge/Hablemos-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:TU-EMAIL)
[![LinkedIn](https://img.shields.io/badge/Conectemos-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/TU-USUARIO/)

</div>
