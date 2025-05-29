---
title: License Class
linktitle: License
articleTitle: License
second_title: Aspose.Words para .NET
description: Desbloquee todo el potencial de Aspose.Words con nuestra clase de licencia. Gestione fácilmente las licencias para un procesamiento de documentos fluido y una funcionalidad mejorada.
type: docs
weight: 3870
url: /es/net/aspose.words/license/
---
## License class

Proporciona métodos para licenciar el componente.

Para obtener más información, visite el[Licencias y suscripciones](https://docs.aspose.com/words/net/licensing/) Artículo de documentación.

```csharp
public class License
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [License](license/)() | Inicializa una nueva instancia de esta clase. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense)(*Stream*) | Licencia el componente. |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense_1)(*string*) | Licencia el componente. |

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
