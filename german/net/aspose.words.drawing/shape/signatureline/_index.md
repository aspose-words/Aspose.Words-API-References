---
title: Shape.SignatureLine
linktitle: SignatureLine
articleTitle: SignatureLine
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie auf das SignatureLine-Objekt für Ihre Formen zugreifen. Identifizieren Sie Signaturzeilen ganz einfach und verleihen Sie Ihrem Dokument mehr Professionalität!
type: docs
weight: 170
url: /de/net/aspose.words.drawing/shape/signatureline/
---
## Shape.SignatureLine property

Ruft ab[`SignatureLine`](../../signatureline/) Objekt, wenn die Form eine Signaturzeile ist. Gibt zurück`null` andernfalls.

```csharp
public SignatureLine SignatureLine { get; }
```

## Bemerkungen

Sie können neue einfügen[`SignatureLine`](../../signatureline/) in das Dokument mit[`InsertSignatureLine`](../../../aspose.words/documentbuilder/insertsignatureline/) und

## Beispiele

Zeigt, wie Sie eine Zeile für eine Signatur erstellen und in ein Dokument einfügen.

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

// Fügen Sie eine Form ein, die eine Signaturzeile enthält, deren Aussehen wir
// Anpassen mithilfe des Objekts „SignatureLineOptions“, das wir oben erstellt haben.
// Wenn wir eine Form einfügen, deren Koordinaten in der unteren rechten Ecke der Seite beginnen,
// Wir müssen negative x- und y-Koordinaten angeben, um die Form sichtbar zu machen.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0,
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// Überprüfen Sie die Eigenschaften unserer Signaturzeile über ihr Shape-Objekt.
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
