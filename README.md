## 1. Integration Service

![Status](https://img.shields.io/badge/status-active-brightgreen)
![License](https://img.shields.io/github/license/tuusuario/datawarehouse-integration)

### 🎥 Demo en Video
<!-- Inserta aquí el enlace al video de demostración -->
[![Demo Integration Service](https://img.youtube.com/vi/VIDEO_ID/0.jpg)](https://youtu.be/VIDEO_ID)

### 📖 Descripción
El **Integration Service** automatiza la extracción, limpieza y carga (ETL) de datos desde orígenes como bases de datos SQL, APIs REST y archivos CSV/JSON. Sus objetivos principales son:

- Conectar con múltiples sistemas de origen.
- Aplicar reglas de calidad y transformación.
- Cargar datos a un Data Lake o Data Warehouse central.

### ⚙️ Características
- Conectores configurables para MySQL, PostgreSQL, MongoDB y APIs.
- Transformaciones basadas en Python (pandas) y SQL.
- Registro de logs y alertas en caso de errores.
- Ejecución programada (cron jobs o Airflow).

### 🛠️ Tecnologías
- **Lenguaje**: Python 3.x
- **Framework**: FastAPI
- **Orquestación**: Apache Airflow
- **Almacenamiento**: AWS S3 / Azure Blob Storage
- **Bases de datos**: MySQL, PostgreSQL, MongoDB

### 🚀 Instalación y Ejecución
```bash
# Clonar repositorio
git clone https://github.com/tuusuario/datawarehouse-integration.git
cd datawarehouse-integration

# Crear entorno virtual
env/bin/activate  # o python -m venv venv && source venv/bin/activate

# Instalar dependencias
pip install -r requirements.txt

# Configurar variables de entorno
export DB_HOST="<host>"
export DB_USER="<user>"
export DB_PASS="<pass>"
export S3_BUCKET="<bucket-name>"

# Iniciar servicio
uvicorn app.main:app --reload
```

### 🔧 Endpoints Principales
| Método | Ruta                    | Descripción                          |
|--------|-------------------------|--------------------------------------|
| GET    | `/health`               | Verifica el estado del servicio      |
| POST   | `/extract/source-name`  | Inicia extracción de datos de origen |
| POST   | `/load/data-target`     | Carga datos al almacenamiento final  |

### 📊 Ejemplo de Flujo ETL
1. `POST /extract/mysql` → Extrae tablas definidas.
2. Transforma datos con reglas en `transforms/`.
3. `POST /load/s3` → Guarda los archivos en S3.

---
