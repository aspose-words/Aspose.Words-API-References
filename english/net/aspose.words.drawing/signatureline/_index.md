---
title: SignatureLine Class
linktitle: SignatureLine
articleTitle: SignatureLine
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Drawing.SignatureLine class to easily manage and customize signature line properties for enhanced document security.
type: docs
weight: 1690
url: /net/aspose.words.drawing/signatureline/
---
## SignatureLine class

Provides access to signature line properties.

To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/net/working-with-digital-signatures/) documentation article.

```csharp
public class SignatureLine
```

## Properties

| Name | Description |
| --- | --- |
| [AllowComments](../../aspose.words.drawing/signatureline/allowcomments/) { get; set; } | Gets or sets a value indicating that the signer can add comments in the Sign dialog. Default value for this property is `false`. |
| [DefaultInstructions](../../aspose.words.drawing/signatureline/defaultinstructions/) { get; set; } | Gets or sets a value indicating that default instructions is shown in the Sign dialog. Default value for this property is `true`. |
| [Email](../../aspose.words.drawing/signatureline/email/) { get; set; } | Gets or sets suggested signer's e-mail address. Default value for this property is **empty string** (Empty). |
| [Id](../../aspose.words.drawing/signatureline/id/) { get; set; } | Gets or sets identifier for this signature line. |
| [Instructions](../../aspose.words.drawing/signatureline/instructions/) { get; set; } | Gets or sets instructions to the signer that are displayed on signing the signature line. This property is ignored if [`DefaultInstructions`](./defaultinstructions/) is set. Default value for this property is **empty string** (Empty). |
| [IsSigned](../../aspose.words.drawing/signatureline/issigned/) { get; } | Indicates that signature line is signed by digital signature. |
| [IsValid](../../aspose.words.drawing/signatureline/isvalid/) { get; } | Indicates that signature line is signed by digital signature and this digital signature is valid. |
| [ProviderId](../../aspose.words.drawing/signatureline/providerid/) { get; set; } | Gets or sets signature provider identifier for this signature line. Default value is "{00000000-0000-0000-0000-000000000000}". |
| [ShowDate](../../aspose.words.drawing/signatureline/showdate/) { get; set; } | Gets or sets a value indicating that sign date is shown in the signature line. Default value for this property is `true`. |
| [Signer](../../aspose.words.drawing/signatureline/signer/) { get; set; } | Gets or sets suggested signer of the signature line. Default value for this property is **empty string** (Empty). |
| [SignerTitle](../../aspose.words.drawing/signatureline/signertitle/) { get; set; } | Gets or sets suggested signer's title (for example, Manager). Default value for this property is **empty string** (Empty). |

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

Assert.That(shape.IsSignatureLine, Is.True);

// Verify the properties of our signature line via its Shape object.
SignatureLine signatureLine = shape.SignatureLine;

Assert.That(signatureLine.Email, Is.EqualTo("john.doe@management.com"));
Assert.That(signatureLine.Signer, Is.EqualTo("John Doe"));
Assert.That(signatureLine.SignerTitle, Is.EqualTo("Senior Manager"));
Assert.That(signatureLine.Instructions, Is.EqualTo("Please sign here"));
Assert.That(signatureLine.ShowDate, Is.True);
Assert.That(signatureLine.AllowComments, Is.True);
Assert.That(signatureLine.DefaultInstructions, Is.True);

doc.Save(ArtifactsDir + "Shape.SignatureLine.docx");
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
