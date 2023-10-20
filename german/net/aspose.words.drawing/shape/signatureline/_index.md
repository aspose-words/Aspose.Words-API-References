---
title: Shape.SignatureLine
linktitle: SignatureLine
articleTitle: SignatureLine
second_title: Aspose.Words für .NET
description: Shape SignatureLine eigendom. Ruft abSignatureLine Objekt wenn die Form eine Signaturlinie ist. Kehrt zurückNull sonst in C#.
type: docs
weight: 160
url: /de/net/aspose.words.drawing/shape/signatureline/
---
## Shape.SignatureLine property

Ruft ab[`SignatureLine`](../../signatureline/) Objekt, wenn die Form eine Signaturlinie ist. Kehrt zurück`Null` sonst.

```csharp
public SignatureLine SignatureLine { get; }
```

## Bemerkungen

Sie können neue einfügen[`SignatureLine`](../../signatureline/) in das Dokument einfügen[`InsertSignatureLine`](../../../aspose.words/documentbuilder/insertsignatureline/) and

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

* class [SignatureLine](../../signatureline/)
* class [Shape](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
