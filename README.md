# Librerías de Runtime de Visual Basic 6.0 (Service Pack 6)

Este repositorio contiene un conjunto de librerías de enlace dinámico (DLL) y librerías de tipos necesarias para ejecutar aplicaciones desarrolladas en **Visual Basic 6.0 (Legacy)**. Estos archivos corresponden al Service Pack 6 (SP6).

## Contenido del Paquete

Los siguientes archivos son componentes esenciales del núcleo de ejecución de VB6:

*   **`msvbvm60.dll`**: La Máquina Virtual de Visual Basic 6.0. Es el archivo principal requerido para ejecutar cualquier programa hecho en VB6.
*   **`oleaut32.dll`**: Librería de Automatización OLE. Maneja operaciones de tipos de datos variantes, fechas y cadenas.
*   **`olepro32.dll`**: Librería de Soporte de Propiedades OLE.
*   **`asycfilt.dll`**: Filtros asíncronos para OLE.
*   **`comcat.dll`**: Component Category Manager.
*   **`stdole2.tlb`**: Librería de tipos estándar OLE.

## Instrucciones de Instalación / Uso

Para que una aplicación legacy funcione correctamente, estos archivos deben estar accesibles para el sistema operativo. Existen dos métodos comunes:

### Método 1: Junto a la aplicación (Recomendado para portabilidad)
Copie todos los archivos de esta carpeta en el mismo directorio donde se encuentra el ejecutable (`.exe`) de su aplicación.

### Método 2: Instalación en el Sistema
Si la aplicación no detecta las librerías localmente, puede copiarlas a los directorios del sistema de Windows:

1.  **Sistemas de 32 bits (x86)**: Copiar a `C:\Windows\System32\`
2.  **Sistemas de 64 bits (x64)**: Copiar a `C:\Windows\SysWOW64\`

**Nota sobre el registro:**
En algunos casos, puede ser necesario registrar las librerías manualmente abriendo una terminal (CMD) como Administrador y ejecutando:
```cmd
regsvr32 msvbvm60.dll
regsvr32 oleaut32.dll
regsvr32 olepro32.dll
```

## Requisitos
*   Sistema Operativo: Windows 98/2000/XP/7/10/11

## Carpetas Adicionales

Además de las librerías sueltas en la raíz, este repositorio incluye los paquetes de instalación originales:

### `VB6 SP6 Files/`
Instaladores independientes del runtime de Visual Basic 6.0 SP6:

*   **`vbrun60sp6.exe`**: Instalador redistribuible del runtime de VB6 (SP6).
*   **`VB6.0-KB290887-X86.exe`**: Actualización de seguridad (KB290887) para el runtime de VB6.
*   **`VBRun60sp6_exe installs Visual Basic 6_0 SP6 run-time files.mht`**: Página de documentación (guardada como MHT) sobre el instalador del runtime.

### `VS6 SP6/`
Contenido completo del **Service Pack 6 de Visual Studio 6.0**, que actualiza Visual Basic 6.0, Visual C++ 6.0 y Visual SourceSafe 6.0:

*   **`Vs6sp6.exe`**: Instalador principal del Service Pack 6 para Visual Studio 6.0.
*   **`setupsp6.exe`** / **`setup.ini`** / **`*.stf`/`*.inf`**: Archivos de configuración y arranque del instalador.
*   **`*.cab`**: Paquetes comprimidos con los binarios actualizados (runtime de VB6, controles ActiveX como MSComCtl, MSFlexGrid, RichTextBox, Winsock, etc.).
*   **`*.h`, `*.idl`, `*.lib`**: Cabeceras y librerías de enlace para desarrollo con ADO/OLE DB (usadas por Visual C++ 6.0).
*   **`readme.htm`** / **`toc.htm`**: Documentación original de Microsoft sobre el contenido y alcance del Service Pack.
*   **`vcredist.exe`**: Redistribuible de Visual C++.

**Nota:** esta carpeta pesa ~130 MB en total; considera usar Git LFS si el repositorio crece más.

## Aviso Legal
Este software es tecnología "Legacy" (antigua) de Microsoft. Se proporciona tal cual para fines de compatibilidad y mantenimiento de sistemas existentes.
