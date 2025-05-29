---
title: PdfPermissions Enum
linktitle: PdfPermissions
articleTitle: PdfPermissions
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.PdfPermissions para controlar el acceso de los usuarios a archivos PDF cifrados. Mejore la seguridad y gestione eficazmente las operaciones con los documentos.
type: docs
weight: 6310
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
| DisallowAll | `0` | No permite ninguna operación en el documento PDF. Este es el valor predeterminado. |
| AllowAll | `FFFF` | Permite todas las operaciones en el documento PDF. |
| ContentCopy | `10` | Copiar o extraer de otro modo texto y gráficos del documento mediante operaciones distintas a las controladas porContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | Extraer texto y gráficos (para facilitar la accesibilidad a usuarios con discapacidades o para otros fines). |
| ModifyContents | `8` | Modificar el contenido del documento mediante operaciones distintas a las controladas por ModifyAnnotations ,FillIn , yDocumentAssembly . |
| ModifyAnnotations | `20` | Agregue o modifique anotaciones de texto, complete campos de formulario interactivos y, siModifyContents is también establece, crea o modifica campos de formulario interactivos (incluidos los campos de firma). |
| FillIn | `100` | Complete los campos de formulario interactivos existentes (incluidos los campos de firma), incluso siModifyContents está despejado. |
| DocumentAssembly | `400` | Ensamblar el documento (insertar, rotar o eliminar páginas y crear elementos de esquema del documento o imágenes en miniatura ), incluso siModifyContents está claro. |
| Printing | `4` | Imprimir el documento (posiblemente no con el nivel de calidad más alto, dependiendo de si HighResolutionPrinting también está configurado). |
| HighResolutionPrinting | `804` | Imprimir el documento en una representación que permita generar una copia digital fiel del contenido PDF, basándose en un algoritmo dependiente de la implementación. Cuando esta bandera está desactivada (y...Printing está configurado), la impresión se limitará a una representación de bajo nivel de la apariencia, posiblemente de calidad degradada. |

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
