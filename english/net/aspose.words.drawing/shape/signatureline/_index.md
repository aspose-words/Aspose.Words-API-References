---
title: Shape.SignatureLine
linktitle: SignatureLine
articleTitle: SignatureLine
second_title: Aspose.Words for .NET
description: Discover how to access the SignatureLine object for your shapes. Easily identify signature lines and enhance your document's professionalism!
type: docs
weight: 170
url: /net/aspose.words.drawing/shape/signatureline/
---
## Shape.SignatureLine property

Gets [`SignatureLine`](../../signatureline/) object if the shape is a signature line. Returns `null` otherwise.

```csharp
public SignatureLine SignatureLine { get; }
```

## Remarks

You can insert new [`SignatureLine`](../../signatureline/) into the document using [`InsertSignatureLine`](../../../aspose.words/documentbuilder/insertsignatureline/) and

## Examples

Shows how to create a line for a signature and insert it into a document.

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

// Insert a shape that will contain a signature line, whose appearance we will
// customize using the "SignatureLineOptions" object we have created above.
// If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
// we will need to supply negative x and y coordinates to bring the shape into view.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0,
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// Verify the properties of our signature line via its Shape object.
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

### See Also

* class [SignatureLine](../../signatureline/)
* class [Shape](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
