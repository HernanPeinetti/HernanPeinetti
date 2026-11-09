<div align="center">

# Hernán Peinetti

### Data Engineer · Python · SQL · Airflow

**Construyo pipelines que corren solos y en los que se puede confiar.**
Ingesta desde APIs y archivos, validación de calidad, modelado en capas y orquestación diaria.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/TU-USUARIO/)
[![Email](https://img.shields.io/badge/Escribime-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:TU-EMAIL)
[![CV](https://img.shields.io/badge/Ver_CV-2ea043?style=for-the-badge&logo=readdotcv&logoColor=white)](TU-LINK-AL-CV)

📍 Argentina · 🟢 Disponible para trabajar · 🌎 Remoto

</div>

---

## 🎯 Proyecto destacado

<div align="center">

### [Pipeline de datos end-to-end →](https://github.com/HernanPeinetti/NOMBRE-DEL-REPO)

*De una API pública a un dashboard confiable, sin tocar nada a mano.*

<!-- GIF del DAG corriendo en Airflow. Esto es lo que más impacta: descomentalo cuando lo tengas.
<img src="docs/pipeline.gif" width="760" alt="DAG de Airflow ejecutándose">
-->

</div>

```mermaid
flowchart LR
    A("🌐 API pública"):::source --> B("⚙️ Airflow<br/><b>extract</b>"):::orch
    B --> C[("🐘 PostgreSQL<br/><b>raw</b>")]:::store
    C --> D("🔧 dbt<br/><b>staging</b>"):::transform
    D --> E("📦 dbt<br/><b>marts</b>"):::transform
    E --> F("📊 Dashboard"):::output
    Q{{"✅ Tests de calidad"}}:::quality -.-> C
    Q -.-> E

    classDef source fill:#1f6feb,stroke:#58a6ff,stroke-width:2px,color:#fff
    classDef orch fill:#017CEE,stroke:#58a6ff,stroke-width:2px,color:#fff
    classDef store fill:#4169E1,stroke:#8b9dff,stroke-width:2px,color:#fff
    classDef transform fill:#FF694B,stroke:#ff9b85,stroke-width:2px,color:#fff
    classDef output fill:#2ea043,stroke:#56d364,stroke-width:2px,color:#fff
    classDef quality fill:#8957e5,stroke:#bc8cff,stroke-width:2px,color:#fff
```

<div align="center">
<table>
<tr>
<td align="center"><b>50k</b><br/><sub>filas / día</sub></td>
<td align="center"><b>~3 min</b><br/><sub>por corrida</sub></td>
<td align="center"><b>12</b><br/><sub>tests de calidad</sub></td>
<td align="center"><b>100%</b><br/><sub>idempotente</sub></td>
<td align="center"><b>1</b><br/><sub>comando para levantarlo</sub></td>
</tr>
</table>
</div>

**Los tres problemas que tuve que resolver:**

| Problema | Cómo lo resolví |
|---|---|
| La API falla de forma intermitente | Reintentos con backoff exponencial; el DAG no se cae ni pierde la ventana del día |
| Re-ejecutar duplicaba datos | Carga idempotente con *merge* por clave natural; correrlo dos veces da el mismo resultado |
| Datos malos llegaban al dashboard | 12 tests de dbt (nulos, duplicados, rangos, integridad referencial) que frenan la publicación |

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
Extrae de archivo o API, valida calidad y carga en un esquema documentado en PostgreSQL.

`Python` `Pandas` `SQL` `PostgreSQL`

</td>
<td width="50%" valign="top">

### 🔄 [Airflow Orchestration](https://github.com/HernanPeinetti/airflow-data-orchestration)
DAG que consume una API pública a diario y la persiste en PostgreSQL, todo con Docker Compose.

`Airflow` `Python` `Docker`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🐳 [Docker + CI Starter](https://github.com/HernanPeinetti/docker-starter)
App containerizada con tests y despliegue automatizado vía GitHub Actions.

`Docker` `GitHub Actions` `Linux`

</td>
<td width="50%" valign="top">

### 🖥️ [SysOps Automation](https://github.com/HernanPeinetti/sysops-automation)
Scripts de backup, rotación de logs y alertas de disco, programados con cron.

`Bash` `Linux` `Cron`

</td>
</tr>
</table>

---

## 🧰 Stack

<div align="center">

**Datos**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

**Infra y DevOps**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

**Desarrollo** *(experiencia previa)*

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)

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

---

## 🌱 Aprendiendo ahora

`PySpark` · `AWS (S3, Glue, Redshift)` · `Modelado dimensional avanzado` · `Testing de datos con Great Expectations`

---

<div align="center">

### ¿Buscás a alguien para tu equipo de datos?

Estoy abierto a oportunidades como Data Engineer junior.

[![Email](https://img.shields.io/badge/Hablemos-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:TU-EMAIL)
[![LinkedIn](https://img.shields.io/badge/Conectemos-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/TU-USUARIO/)

</div>
