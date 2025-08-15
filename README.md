# App-python

## Estado de CI/CD

| Workflow           | Estado (rama main)                                                                                                         |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------- |
| **CI Básico**      | [![CI Básico Python](https://github.com/FranciscoJTHG/App-python/actions/workflows/ci-python.yml/badge.svg?branch=main)](https://github.com/FranciscoJTHG/App-python/actions/workflows/ci-python.yml)          |
| **CI Matriz**      | [![CI Python Matrix](https://github.com/FranciscoJTHG/App-python/actions/workflows/ci-matrix.yml/badge.svg?branch=main)](https://github.com/FranciscoJTHG/App-python/actions/workflows/ci-matrix.yml)        |
| **Build Docker**   | [![Build Docker](https://github.com/FranciscoJTHG/App-python/actions/workflows/docker-build.yml/badge.svg?branch=main)](https://github.com/FranciscoJTHG/App-python/actions/workflows/docker-build.yml) |

Aplicación web simple desarrollada con Flask.

## Características

*   **API REST:** Expone varios endpoints para diferentes funcionalidades.
*   **Testing:** Incluye una suite de tests con pytest.
*   **Integración Continua:** Configuración de GitHub Actions para CI.

## Endpoints

*   `GET /`: Mensaje de bienvenida.
*   `GET /health`: Verifica el estado de la aplicación.
*   `GET /suma/<int:a>/<int:b>`: Suma dos números enteros.
*   `GET /saludo/<nombre>`: Devuelve un saludo personalizado.

## Cómo empezar

### Prerrequisitos

*   Python 3.9 o superior
*   pip

### Instalación

1.  Clona el repositorio:
    ```bash
    git clone https://github.com/FranciscoJTHG/App-python.git
    ```
2.  Navega al directorio del proyecto:
    ```bash
    cd App-python
    ```
3.  Instala las dependencias:
    ```bash
    pip install -r requirements.txt
    ```

## Ejecutar la aplicación

```bash
python app.py
```

La aplicación estará disponible en `http://localhost:5000`.

## Ejecutar los tests

```bash
pytest
```

## CI/CD

El proyecto utiliza GitHub Actions para la integración continua. Los workflows se encuentran en el directorio `.github/workflows`.

*   `ci-python.yml`: Ejecuta los tests y la cobertura de código en cada push a `master` y `develop`.
*   `ci-matrix.yml`: Ejecuta los tests en diferentes versiones de Python.

## Construido con

*   [Flask](https://flask.palletsprojects.com/) - El framework web utilizado.
*   [Pytest](https://docs.pytest.org/) - Para los tests.
