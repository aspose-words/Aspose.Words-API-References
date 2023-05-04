---
title: SignatureLine.Email
linktitle: Email
articleTitle: Email
second_title: Aspose.Words for .NET
description: SignatureLine Email property. Gets or sets suggested signers email address. Default value for this property is empty string Empty in C#.
type: docs
weight: 30
url: /net/aspose.words.drawing/signatureline/email/
---
## SignatureLine.Email property

Gets or sets suggested signer's e-mail address. Default value for this property is **empty string** (Empty).

```csharp
public string Email { get; set; }
```

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

* class [SignatureLine](../)
* namespace [Aspose.Words.Drawing](../../signatureline/)
* assembly [Aspose.Words](../../../)
