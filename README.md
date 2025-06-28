![License](https://img.shields.io/github/license/tuusuario/datawarehouse-integration)
![Status](https://img.shields.io/badge/status-beta-yellow) ![License](https://img.shields.io/github/license/AxelSuazoContent/ANALISIS_SERVICE_PROYECT)

---

## 🎥 Demo en Video
<!-- Inserta aquí el enlace al video de demostración -->
[![Demo Analysis Service]([https://img.youtube.com/vi/VIDEO_ID/0.jpg)](https://youtu.be/VIDEO_ID](https://youtu.be/y63FWkAt_o0))

---

## 📖 Descripción
El **Analysis Service** ofrece una API REST para consultas analíticas, visualización y generación de reportes (PDF/CSV) sobre los datos consolidados en el Data Warehouse.

---

## 📂 Estructura de Carpetas
```
ANALISIS_SERVICE_PROYECT/
├─ .gitattributes
├─ .gitignore
├─ proyectobd2.sln
└─ AnalysisService/
   ├─ Controllers/
   ├─ Models/
   ├─ Services/
   └─ appsettings.json
```

---

## ⚙️ Características Destacadas
- Endpoints con filtros de fecha y paginación.
- Generación de reportes programados.
- Autenticación JWT y gestión de roles.
- Frontend opcional con React/Chart.js.

---

## 🚀 Instalación y Ejecución
```bash
# Clonar el repositorio
git clone https://github.com/AxelSuazoContent/ANALISIS_SERVICE_PROYECT.git
cd ANALISIS_SERVICE_PROYECT

# Restaurar y compilar
dotnet restore proyectobd2.sln
dotnet build proyectobd2.sln

# Ejecutar el servicio
dotnet run --project AnalysisService/AnalysisService.csproj
```

---

## 🔧 Configuración (appsettings.json)
```jsonc
{
  "ConnectionStrings": {
    "WarehouseDB": "Server=<host>;Database=<warehouse>;User Id=<user>;Password=<pass>;"
  },
  "Jwt": {
    "Key": "TuSecretoSuperSecreto",
    "Issuer": "AnalysisService",
    "Audience": "DataWerHauseUsers"
  }
}
```

---

## 🤝 Contribuciones
Las contribuciones son bienvenidas: abre un _issue_ o _pull request_.

## 📄 Licencia
MIT License

---

_Desarrollado por Axel Gerónimo (axelgeronimo0@gmail.com)_

