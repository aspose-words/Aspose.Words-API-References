---
title: License.License
second_title: Referencia de API de Aspose.Words para .NET
description: License constructor. Inicializa una nueva instancia de esta clase.
type: docs
weight: 10
url: /es/net/aspose.words/license/license/
---
## License constructor

Inicializa una nueva instancia de esta clase.

```csharp
public License()
```

### Ejemplos

Muestra cómo inicializar una licencia para Aspose.Words usando un archivo de licencia en el sistema de archivos local.

```csharp
// Configure la licencia para nuestro producto Aspose.Words pasando el nombre de archivo del sistema de archivos local de un archivo de licencia válido.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Crea una copia de nuestro archivo de licencia en la carpeta de binarios de nuestra aplicación.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Si pasamos el nombre de un archivo sin ruta,
// SetLicense buscará este archivo en varias ubicaciones del sistema de archivos local.
// Una de esas ubicaciones será la carpeta "bin", que contiene una copia de nuestro archivo de licencia.
license.SetLicense("Aspose.Words.NET.lic");
```

### Ver también

* class [License](../)
* espacio de nombres [Aspose.Words](../../license/)
* asamblea [Aspose.Words](../../../)


