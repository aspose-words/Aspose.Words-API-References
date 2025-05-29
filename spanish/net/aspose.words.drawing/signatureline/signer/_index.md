---
title: SignatureLine.Signer
linktitle: Signer
articleTitle: Signer
second_title: Aspose.Words para .NET
description: Mejore sus documentos con la propiedad Firmante de SignatureLine. Configure fácilmente firmantes sugeridos para las líneas de firma, optimizando su proceso de firma sin esfuerzo.
type: docs
weight: 100
url: /es/net/aspose.words.drawing/signatureline/signer/
---
## SignatureLine.Signer property

Obtiene o establece el firmante sugerido de la línea de firma. El valor predeterminado para esta propiedad es**cadena vacía** (Empty ).

```csharp
public string Signer { get; set; }
```

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

* class [SignatureLine](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
