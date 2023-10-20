---
title: SignatureLine.Instructions
linktitle: Instructions
articleTitle: Instructions
second_title: Aspose.Words für .NET
description: SignatureLine Instructions eigendom. Ruft Anweisungen an den Unterzeichner ab oder legt diese fest die beim Signieren der Signaturzeile angezeigt werden. Diese Eigenschaft wird ignoriert wennDefaultInstructionsist set. Der Standardwert für diese Eigenschaft istleerer String Empty in C#.
type: docs
weight: 50
url: /de/net/aspose.words.drawing/signatureline/instructions/
---
## SignatureLine.Instructions property

Ruft Anweisungen an den Unterzeichner ab oder legt diese fest, die beim Signieren der Signaturzeile angezeigt werden. Diese Eigenschaft wird ignoriert, wenn[`DefaultInstructions`](../defaultinstructions/)ist set. Der Standardwert für diese Eigenschaft ist**leerer String** (Empty).

```csharp
public string Instructions { get; set; }
```

## Beispiele

Zeigt, wie eine Zeile für eine Signatur erstellt und in ein Dokument eingefügt wird.

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

// Fügen Sie eine Form ein, die eine Signaturlinie enthält, deren Aussehen wir festlegen
// Anpassen mit dem „SignatureLineOptions“-Objekt, das wir oben erstellt haben.
// Wenn wir eine Form einfügen, deren Koordinaten aus der unteren rechten Ecke der Seite stammen,
// Wir müssen negative X- und Y-Koordinaten angeben, um die Form sichtbar zu machen.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0, 
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// Überprüfen Sie die Eigenschaften unserer Signaturlinie über ihr Shape-Objekt.
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

### Siehe auch

* class [SignatureLine](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
