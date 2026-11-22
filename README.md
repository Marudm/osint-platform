# 🔍 OSINT Intelligence Platform

![Python](https://img.shields.io/badge/Python-3.13-blue) ![Django](https://img.shields.io/badge/Django-4.2-green) ![License](https://img.shields.io/badge/License-MIT-yellow)

Plataforma de inteligencia OSINT desarrollada con Django y Python, orientada a tareas de análisis de seguridad, threat intelligence y operaciones SOC.

## 🚀 Features

- 🌐 **IP Intelligence** — geolocalización, ASN, ISP, reverse DNS y escaneo básico de puertos comunes
- 🚨 **Threat Intelligence** — integración con AbuseIPDB para abuse score en tiempo real
- 🗺️ **Mapa interactivo** — geolocalización visual con Leaflet.js
- ⚠️ **Risk Score automático** — calculado en base a múltiples indicadores
- 🔎 **Hallazgos OSINT** — detección automática de indicadores de riesgo
- 📋 **Export JSON** — resultados exportables para análisis externo

## 🛠️ Stack Tecnológico

| Categoría    | Tecnología                 |
| ------------ | -------------------------- |
| Backend      | Python 3.13, Django 4.2    |
| Frontend     | HTML5, CSS3, JavaScript    |
| APIs         | AbuseIPDB, ip-api.com      |
| Mapas        | Leaflet.js + OpenStreetMap |
| Herramientas | Git, VS Code               |

## ⚙️ Instalación

```bash
git clone https://github.com/Marudm/claude-osint.git
cd claude-osint
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

Accedé a `http://127.0.0.1:8000` en tu navegador.

## 🔑 Configuración de la API key

Para activar el análisis de abuso en tiempo real, registrate gratis en [AbuseIPDB](https://www.abuseipdb.com/register) y creá tu archivo `.env`:

```bash
copy .env.example .env      # Linux/Mac: cp .env.example .env
```

Editá `.env` y pegá tu key, sin comillas ni espacios:

```
ABUSEIPDB_API_KEY=tu_key
```

El archivo `.env` está en el `.gitignore` y no se sube al repositorio. Si la key no está configurada, la app lo avisa en los resultados en vez de mostrar la IP como limpia.

## ⚠️ Uso responsable

La función de escaneo de puertos intenta conexiones TCP al objetivo. Usala **solo sobre sistemas propios o con autorización expresa**. El escaneo de sistemas ajenos sin permiso puede ser ilegal.

## 🎯 Casos de Uso

- Análisis de IPs sospechosas en incidentes de seguridad
- Threat intelligence para equipos SOC
- Investigación OSINT de infraestructura maliciosa
- Enriquecimiento de IOCs durante respuesta a incidentes

## 👩‍💻 Autora

**Marina Andrea Della Mattia**

- 🔗 [LinkedIn](https://linkedin.com/in/marinadellamattia)
- 🐙 [GitHub](https://github.com/Marudm)
- 📧 [marinadellamattia.estudio@gmail.com](mailto:marinadellamattia.estudio@gmail.com)