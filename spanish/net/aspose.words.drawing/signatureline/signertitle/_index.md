---
title: SignatureLine.SignerTitle
linktitle: SignerTitle
articleTitle: SignerTitle
second_title: Aspose.Words para .NET
description: Personalice el Título del Firmante en SignatureLine para optimizar el flujo de trabajo de sus documentos. Configure títulos sugeridos como "Administrador" para una experiencia de firma optimizada.
type: docs
weight: 110
url: /es/net/aspose.words.drawing/signatureline/signertitle/
---
## SignatureLine.SignerTitle property

Obtiene o establece el título sugerido del firmante (por ejemplo, Gerente). El valor predeterminado para esta propiedad es**cadena vacía** (Empty ).

```csharp
public string SignerTitle { get; set; }
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
