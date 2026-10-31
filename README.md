<div align="center">

# Práctica — Modelos y Roles con SQLAlchemy

[![Python](https://img.shields.io/badge/Python-3.12-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-3.x-000000?logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-2.x-D71F00?logo=sqlalchemy&logoColor=white)](https://www.sqlalchemy.org/)
[![Licencia: MIT](https://img.shields.io/badge/Licencia-MIT-yellow.svg)](LICENSE)

Práctica de modelos relacionales con SQLAlchemy: usuarios con roles, catálogo de
canciones, álbumes y medios.

</div>

---

## Descripción

Ejercicio de clase sobre relaciones entre entidades y control de acceso por roles.
Cada usuario pertenece a un rol, y el catálogo musical se modela con álbumes,
canciones y formatos de publicación.

## Modelo de datos

| Modelo | Tabla | Propósito |
| :--- | :--- | :--- |
| `Usuario` | `usuarios` | Cuenta del sistema, asociada a un rol |
| `Rol` | `roles` | Perfil de permisos del usuario |
| `Album` | `albumes` | Agrupación de canciones |
| `Cancion` | `canciones` | Tema musical |
| `AlbumCancion` | `album_cancion` | Tabla intermedia álbum ↔ canción |
| `Medio` | `medios` | Formato de publicación |

## Estructura

```
app/
├── config/settings.py        Configuración y cadena de conexión
├── database/database.py      Instancia de SQLAlchemy
└── models/                   Un archivo por entidad
run.py                        Punto de entrada
```

## Cómo ejecutarlo

```bash
python -m venv venv
venv\Scripts\activate         # Windows
pip install -r requirements.txt
python run.py
```

## Autor

**Sara Garzón** · [github.com/sara051106garzon-boop](https://github.com/sara051106garzon-boop)

## Licencia

Este proyecto está bajo la licencia [MIT](LICENSE).
