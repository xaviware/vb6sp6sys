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

## Aviso Legal
Este software es tecnología "Legacy" (antigua) de Microsoft. Se proporciona tal cual para fines de compatibilidad y mantenimiento de sistemas existentes.
