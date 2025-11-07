# 💾 Aplicación CRUD de Escritorio con C# y SQLite

Este repositorio contiene una aplicación de escritorio simple construida con **C# y Windows Forms** que implementa las operaciones básicas **CRUD** (Crear, Leer, Actualizar, Eliminar) para la gestión de registros de personas. La aplicación utiliza la base de datos local **SQLite** para la persistencia de datos.

## 🌟 Características Principales

* **Aplicación de Escritorio:** Desarrollada con la biblioteca **Windows Forms** de .NET.
* **CRUD Completo:** Permite a los usuarios agregar, visualizar, modificar y eliminar registros de la entidad `Persona` (Nombre y Edad).
* **Persistencia Local con SQLite:** Utiliza una base de datos **SQLite** (`miBaseDeDatos.db`) para almacenar los datos de forma local. La tabla `Personas` se inicializa automáticamente al iniciar la aplicación.
* **Capa de Acceso a Datos (DAL):** El código sigue un patrón de separación de responsabilidades, con una clase `DataAccess` dedicada a manejar toda la interacción SQL.

## 🛠️ Tecnologías Utilizadas

* **Lenguaje:** C#
* **Plataforma:** .NET (Windows Forms Application)
* **Base de Datos:** SQLite
* **Paquetes NuGet Clave:** `System.Data.SQLite`

## 📂 Estructura del Código

| Archivo | Responsabilidad |
| :--- | :--- |
| `Persona.cs` | **Modelo de Datos.** Define la estructura de la entidad `Persona` (Id, Nombre, Edad). |
| `DataAccess.cs` | **Capa de Datos (DAL).** Contiene la lógica de conexión a SQLite y todos los métodos CRUD (SELECT, INSERT, UPDATE, DELETE). |
| `Form1.cs` | **Lógica UI.** Maneja los eventos de los botones, carga los datos en el `DataGridView` y se comunica con la capa `DataAccess`. |

## 💻 Puesta en Marcha

Para compilar y ejecutar este proyecto, necesitas el SDK de .NET y Visual Studio.

1.  **Requisitos:** Tener instalado el **SDK de .NET** y **Visual Studio** (con la carga de trabajo de Desarrollo de escritorio .NET).
2.  **Clonar el repositorio:**
    ```bash
    git clone [URL_DE_TU_REPOSITORIO]
    cd [NombreDeTuCarpeta]
    ```
3.  **Restaurar Paquetes NuGet:**
    ```bash
    dotnet restore
    ```
4.  **Ejecutar la Aplicación:**
    ```bash
    dotnet run
    ```

> **Nota:** La base de datos (`miBaseDeDatos.db`) se creará automáticamente la primera vez que la aplicación se ejecute en el directorio de salida (bin/Debug/...).

## 📚 Uso de la Aplicación

Los botones realizan las siguientes acciones:

* **Create (Crear):** Agrega un nuevo registro con el Nombre y Edad de los campos de texto.
* **Update (Actualizar):** Modifica la fila seleccionada en el `DataGridView` con los datos de los campos de texto.
* **Delete (Eliminar):** Elimina el registro de la fila seleccionada del `DataGridView`.

---

¿Hay algún otro `README.md` o documentación que necesites generar o revisar para alguno de tus proyectos?
