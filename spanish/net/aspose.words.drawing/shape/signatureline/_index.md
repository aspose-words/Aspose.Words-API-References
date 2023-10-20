---
title: Shape.SignatureLine
linktitle: SignatureLine
articleTitle: SignatureLine
second_title: Aspose.Words para .NET
description: Shape SignatureLine propiedad. ObtieneSignatureLine objeto si la forma es una línea de firma. Devolucionesnulo de lo contrario en C#.
type: docs
weight: 160
url: /es/net/aspose.words.drawing/shape/signatureline/
---
## Shape.SignatureLine property

Obtiene[`SignatureLine`](../../signatureline/) objeto si la forma es una línea de firma. Devoluciones`nulo` de lo contrario.

```csharp
public SignatureLine SignatureLine { get; }
```

## Observaciones

Puedes insertar nuevos[`SignatureLine`](../../signatureline/) en el documento usando[`InsertSignatureLine`](../../../aspose.words/documentbuilder/insertsignatureline/) y

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

// Inserta una forma que contendrá una línea de firma, cuya apariencia configuraremos
// personalizar usando el objeto "SignatureLineOptions" que hemos creado arriba.
// Si insertamos una forma cuyas coordenadas se originan en la esquina inferior derecha de la página,
// necesitaremos proporcionar coordenadas xey negativas para que la forma se vea.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0, 
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// Verifica las propiedades de nuestra línea de firma a través de su objeto Shape.
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

* class [SignatureLine](../../signatureline/)
* class [Shape](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
