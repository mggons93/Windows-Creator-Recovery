# Windows Recovery using HDD / Recuperación de Windows usando HDD

## Imagen de Muestra / Sample Image
<p align="center">
<a href=></a><img src="https://i.ibb.co/VWC8fJZf/Captura-de-pantalla-2025-06-04-165954.png"/>
</p>

## Imagen de Muestra / Sample Image
<p align="center">
<a href=></a><img src="https://i.ibb.co/cSSBFtHY/Captura-de-pantalla-2025-06-04-165912.png"/>
</p>


## Español

### Descripción

Esta utilidad permite crear o restaurar un entorno de recuperación de Windows directamente en el disco duro local, especialmente útil cuando no se dispone de medios externos como USB o DVD. El script ofrece una interfaz gráfica sencilla para seleccionar la partición de destino y la imagen ISO de Windows, automatizando todo el proceso de preparación y configuración del entorno de recuperación.

---

### Características

- **Selección de partición destino:** Permite elegir la partición donde se creará/restaurará el entorno de recuperación.
- **Gestión automatizada de particiones Recovery/WinRE:** Elimina particiones antiguas, extiende la partición principal y crea una nueva partición de recuperación (~7.5 GB), formateada y configurada según el tipo de disco (GPT/MBR).
- **Montaje y copia desde ISO:** Monta una imagen ISO de Windows 10/11 y copia los archivos necesarios a la partición de recuperación, excluyendo archivos grandes innecesarios.
- **Actualización de archivos críticos:** Descarga y reemplaza automáticamente el archivo `boot.wim` con controladores NVMe según la versión detectada, y el archivo `autounattend.xml` para automatizar la instalación.
- **Configuración del gestor de arranque:** Crea una nueva entrada en el BCD para arrancar desde la partición de recuperación, detectando automáticamente si el sistema es UEFI o BIOS Legacy.
- **Restauración de WinRE:** Permite restaurar el entorno de recuperación original descargando y aplicando el archivo `winre.wim` adecuado según la versión de Windows.
- **Bitácora y mensajes de estado:** Todas las operaciones quedan registradas en el log de la interfaz.

---

### Opciones disponibles

- Instalar Recovery desde ISO.
- Remontar WinRE original.
- Remontar partición Recovery existente.

---

### Requisitos

- PowerShell con módulos de administración de discos (`Storage`).
- Imagen ISO válida de Windows 10 o 11.
- Acceso a Internet para descargar archivos críticos.

---

### Advertencia

> **Utilice esta herramienta bajo su propia responsabilidad. Modifica particiones y el gestor de arranque, lo que puede afectar el funcionamiento del sistema.**

---

## English

### Overview

This utility allows you to create or restore a Windows recovery environment directly on your local hard drive, ideal for situations where you do not have access to external media (USB/DVD). The script provides a simple graphical interface to select the target partition and Windows ISO image, automating the entire process of preparing and configuring the recovery environment.

---

### Features

- **Target partition selection:** Choose the partition where the recovery environment will be created or restored.
- **Automated Recovery/WinRE partition management:** Deletes old recovery partitions, extends the main partition, and creates a new ~7.5 GB recovery partition, formatted and configured according to disk type (GPT/MBR).
- **ISO mounting and file copy:** Mounts a Windows 10/11 ISO and copies the necessary files to the recovery partition, excluding unnecessary large files.
- **Critical file updates:** Automatically downloads and replaces the `boot.wim` file with NVMe drivers based on the detected version, and the `autounattend.xml` file for automated installation.
- **Boot manager configuration:** Creates a new BCD entry to boot from the recovery partition, automatically detecting if the system is UEFI or Legacy BIOS.
- **WinRE restoration:** Allows restoring the original recovery environment by downloading and applying the appropriate `winre.wim` file according to the Windows version.
- **Log and status messages:** All operations are logged in the interface log.

---

### Available Options

- Install Recovery from ISO.
- Remount original WinRE.
- Remount existing Recovery partition.

---

### Requirements

- PowerShell with disk management modules (`Storage`).
- Valid Windows 10 or 11 ISO image.
- Internet access to download critical files.

---

### Warning

> **Use this tool at your own risk. It modifies partitions and the boot manager, which can affect system functionality.**

---
**Author / Autor:** Soporte y Aportes / Mggons
---
**Version / Versión:** 1.7
