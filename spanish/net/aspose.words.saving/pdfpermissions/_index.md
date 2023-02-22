---
title: Enum PdfPermissions
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.PdfPermissions enumeración. Especifica las operaciones que se permiten a un usuario en un documento PDF cifrado.
type: docs
weight: 5230
url: /es/net/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enumeration

Especifica las operaciones que se permiten a un usuario en un documento PDF cifrado.

```csharp
[Flags]
public enum PdfPermissions
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| DisallowAll | `0` | Deshabilita todas las operaciones en el documento PDF. Este es el valor predeterminado. |
| AllowAll | `FFFF` | Permite todas las operaciones sobre el documento PDF. |
| ContentCopy | `10` | Copiar o extraer texto y gráficos del documento mediante operaciones distintas a las controladas porContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | Extraer texto y gráficos (en apoyo de la accesibilidad para usuarios con discapacidades o para otros fines). |
| ModifyContents | `8` | Modificar el contenido del documento mediante operaciones distintas a las controladas por ModifyAnnotations ,FillIn , yDocumentAssembly . |
| ModifyAnnotations | `20` | Agregar o modificar anotaciones de texto, completar campos de formulario interactivo y, siModifyContents is también establece, crea o modifica campos de formulario interactivo (incluidos los campos de firma). |
| FillIn | `100` | Complete los campos de formulario interactivo existentes (incluidos los campos de firma), incluso siModifyContents está claro. |
| DocumentAssembly | `400` | Reúna el documento (inserte, gire o elimine páginas y cree elementos de contorno del documento o imágenes en miniatura ), incluso siModifyContents está claro. |
| Printing | `4` | Imprime el documento (posiblemente no con el nivel de calidad más alto, dependiendo de si HighResolutionPrintingtambién está configurado). |
| HighResolutionPrinting | `804` | Imprime el documento en una representación a partir de la cual se podría generar una copia digital fiel del contenido del PDF , en función de un algoritmo dependiente de la implementación. Cuando esta bandera está clara (and Printing está configurado), la impresión se limitará a una representación de bajo nivel de la apariencia, posiblemente de calidad degradada. |

### Ejemplos

Muestra cómo establecer permisos en un documento PDF guardado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty);

// Comience por desautorizar todos los permisos.
encryptionDetails.Permissions = PdfPermissions.DisallowAll;

// Ampliar permisos para permitir la edición de anotaciones.
encryptionDetails.Permissions = PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly;

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Habilite el cifrado a través de la propiedad "EncryptionDetails".
saveOptions.EncryptionDetails = encryptionDetails;

// Cuando abramos este documento, necesitaremos proporcionar la contraseña antes de acceder a su contenido.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


