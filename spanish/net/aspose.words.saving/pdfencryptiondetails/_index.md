---
title: PdfEncryptionDetails Class
linktitle: PdfEncryptionDetails
articleTitle: PdfEncryptionDetails
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.PdfEncryptionDetails para un cifrado de PDF seguro y permisos de acceso personalizables, garantizando que sus documentos permanezcan protegidos.
type: docs
weight: 6250
url: /es/net/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class

Contiene detalles para cifrar y otorgar permisos de acceso a un documento PDF.

Para obtener más información, visite el[Proteger o cifrar un documento](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) Artículo de documentación.

```csharp
public class PdfEncryptionDetails
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor)(*string, string*) | Inicializa una instancia de esta clase. |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor_1)(*string, string, [PdfPermissions](../pdfpermissions/)*) | Inicializa una instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [OwnerPassword](../../aspose.words.saving/pdfencryptiondetails/ownerpassword/) { get; set; } | Especifica la contraseña del propietario del documento PDF cifrado. |
| [Permissions](../../aspose.words.saving/pdfencryptiondetails/permissions/) { get; set; } | Especifica las operaciones que se permiten a un usuario en un documento PDF cifrado. El valor predeterminado esDisallowAll . |
| [UserPassword](../../aspose.words.saving/pdfencryptiondetails/userpassword/) { get; set; } | Especifica la contraseña de usuario necesaria para abrir el documento PDF cifrado. |

## Ejemplos

Muestra cómo establecer permisos en un documento PDF guardado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

//Ampliar los permisos para permitir la edición de anotaciones.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Habilite el cifrado a través de la propiedad "EncryptionDetails".
saveOptions.EncryptionDetails = encryptionDetails;

//Cuando abramos este documento, necesitaremos proporcionar la contraseña antes de acceder a su contenido.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
