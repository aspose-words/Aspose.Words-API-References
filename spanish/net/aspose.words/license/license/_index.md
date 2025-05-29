---
title: License
linktitle: License
articleTitle: License
second_title: Aspose.Words para .NET
description: Cree y administre licencias fácilmente con nuestra clase constructora. ¡Simplifique su proceso de licencias y mejore su eficiencia hoy mismo!
type: docs
weight: 10
url: /es/net/aspose.words/license/license/
---
## License constructor

Inicializa una nueva instancia de esta clase.

```csharp
public License()
```

## Ejemplos

Muestra cómo inicializar una licencia para Aspose.Words utilizando un archivo de licencia en el sistema de archivos local.

```csharp
// Establezca la licencia para nuestro producto Aspose.Words pasando el nombre del archivo del sistema de archivos local de un archivo de licencia válido.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Cree una copia de nuestro archivo de licencia en la carpeta binarios de nuestra aplicación.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Si pasamos el nombre de un archivo sin una ruta,
// SetLicense buscará este archivo en varias ubicaciones del sistema de archivos local.
// Una de esas ubicaciones será la carpeta "bin", que contiene una copia de nuestro archivo de licencia.
license.SetLicense("Aspose.Words.NET.lic");
```

### Ver también

* class [License](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
