---
title: SignatureLine Class
linktitle: SignatureLine
articleTitle: SignatureLine
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.SignatureLine para administrar y personalizar fácilmente las propiedades de la línea de firma para una mayor seguridad del documento.
type: docs
weight: 1700
url: /es/net/aspose.words.drawing/signatureline/
---
## SignatureLine class

Proporciona acceso a las propiedades de la línea de firma.

Para obtener más información, visite el[Trabajar con firmas digitales](https://docs.aspose.com/words/net/working-with-digital-signatures/) Artículo de documentación.

```csharp
public class SignatureLine
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AllowComments](../../aspose.words.drawing/signatureline/allowcomments/) { get; set; } | Obtiene o establece un valor que indica que el firmante puede agregar comentarios en el cuadro de diálogo Firmar. El valor predeterminado para esta propiedad es`FALSO` . |
| [DefaultInstructions](../../aspose.words.drawing/signatureline/defaultinstructions/) { get; set; } | Obtiene o establece un valor que indica que las instrucciones predeterminadas se muestran en el cuadro de diálogo Firmar. El valor predeterminado para esta propiedad es`verdadero` . |
| [Email](../../aspose.words.drawing/signatureline/email/) { get; set; } | Obtiene o establece la dirección de correo electrónico del firmante sugerido. El valor predeterminado para esta propiedad es**cadena vacía** (Empty ). |
| [Id](../../aspose.words.drawing/signatureline/id/) { get; set; } | Obtiene o establece el identificador para esta línea de firma. |
| [Instructions](../../aspose.words.drawing/signatureline/instructions/) { get; set; } | Obtiene o establece instrucciones para el firmante que se muestran al firmar la línea de firma. Esta propiedad se ignora si[`DefaultInstructions`](./defaultinstructions/) se establece. El valor predeterminado para esta propiedad es**cadena vacía** (Empty ). |
| [IsSigned](../../aspose.words.drawing/signatureline/issigned/) { get; } | Indica que la línea de firma está firmada mediante firma digital. |
| [IsValid](../../aspose.words.drawing/signatureline/isvalid/) { get; } | Indica que la línea de firma está firmada mediante firma digital y esta firma digital es válida. |
| [ProviderId](../../aspose.words.drawing/signatureline/providerid/) { get; set; } | Obtiene o establece el identificador del proveedor de firma para esta línea de firma. El valor predeterminado es "{00000000-0000-0000-0000-000000000000}". |
| [ShowDate](../../aspose.words.drawing/signatureline/showdate/) { get; set; } | Obtiene o establece un valor que indica que la fecha de la firma se muestra en la línea de firma. El valor predeterminado para esta propiedad es`verdadero` . |
| [Signer](../../aspose.words.drawing/signatureline/signer/) { get; set; } | Obtiene o establece el firmante sugerido de la línea de firma. El valor predeterminado para esta propiedad es**cadena vacía** (Empty ). |
| [SignerTitle](../../aspose.words.drawing/signatureline/signertitle/) { get; set; } | Obtiene o establece el título sugerido del firmante (por ejemplo, Gerente). El valor predeterminado para esta propiedad es**cadena vacía** (Empty ). |

## Ejemplos

Muestra cómo crear una línea para una firma e insertarla en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions options = new SignatureLineOptions
{
    AllowComments = true,
    DefaultInstructions = true,
    Email = "john.doe@management.com",
    Instructions = "Please sign here",
    ShowDate = true,
    Signer = "John Doe",
    SignerTitle = "Senior Manager"
};

// Insertar una forma que contendrá una línea de firma, cuya apariencia definiremos
// personaliza usando el objeto "SignatureLineOptions" que hemos creado anteriormente.
// Si insertamos una forma cuyas coordenadas se originan en la esquina inferior derecha de la página,
// Necesitaremos proporcionar coordenadas x e y negativas para que la forma sea visible.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0,
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// Verifique las propiedades de nuestra línea de firma a través de su objeto Shape.
SignatureLine signatureLine = shape.SignatureLine;

Assert.AreEqual("john.doe@management.com", signatureLine.Email);
Assert.AreEqual("John Doe", signatureLine.Signer);
Assert.AreEqual("Senior Manager", signatureLine.SignerTitle);
Assert.AreEqual("Please sign here", signatureLine.Instructions);
Assert.True(signatureLine.ShowDate);
Assert.True(signatureLine.AllowComments);
Assert.True(signatureLine.DefaultInstructions);

doc.Save(ArtifactsDir + "Shape.SignatureLine.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
