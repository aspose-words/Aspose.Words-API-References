---
title: SignatureLine Class
linktitle: SignatureLine
articleTitle: SignatureLine
second_title: Aspose.Words für .NET
description: Aspose.Words.Drawing.SignatureLine klas. Bietet Zugriff auf die Eigenschaften der Signaturzeile in C#.
type: docs
weight: 1300
url: /de/net/aspose.words.drawing/signatureline/
---
## SignatureLine class

Bietet Zugriff auf die Eigenschaften der Signaturzeile.

Um mehr zu erfahren, besuchen Sie die[Arbeiten Sie mit digitalen Signaturen](https://docs.aspose.com/words/net/working-with-digital-signatures/) Dokumentationsartikel.

```csharp
public class SignatureLine
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowComments](../../aspose.words.drawing/signatureline/allowcomments/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der angibt, dass der Unterzeichner im Dialogfeld „Signieren“ Kommentare hinzufügen kann. Der Standardwert für diese Eigenschaft ist`FALSCH` . |
| [DefaultInstructions](../../aspose.words.drawing/signatureline/defaultinstructions/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der angibt, dass Standardanweisungen im Dialogfeld „Signieren“ angezeigt werden. Der Standardwert für diese Eigenschaft ist`WAHR` . |
| [Email](../../aspose.words.drawing/signatureline/email/) { get; set; } | Ruft die E-Mail-Adresse des vorgeschlagenen Unterzeichners ab oder legt diese fest. Der Standardwert für diese Eigenschaft ist**leerer String** (Empty). |
| [Id](../../aspose.words.drawing/signatureline/id/) { get; set; } | Ruft die Kennung für diese Signaturzeile ab oder legt diese fest. |
| [Instructions](../../aspose.words.drawing/signatureline/instructions/) { get; set; } | Ruft Anweisungen an den Unterzeichner ab oder legt diese fest, die beim Signieren der Signaturzeile angezeigt werden. Diese Eigenschaft wird ignoriert, wenn[`DefaultInstructions`](./defaultinstructions/)ist set. Der Standardwert für diese Eigenschaft ist**leerer String** (Empty). |
| [IsSigned](../../aspose.words.drawing/signatureline/issigned/) { get; } | Zeigt an, dass die Signaturzeile mit einer digitalen Signatur signiert ist. |
| [IsValid](../../aspose.words.drawing/signatureline/isvalid/) { get; } | Zeigt an, dass die Signaturzeile mit einer digitalen Signatur signiert ist und diese digitale Signatur gültig ist. |
| [ProviderId](../../aspose.words.drawing/signatureline/providerid/) { get; set; } | Ruft die Signaturanbieter-ID für diese Signaturzeile ab oder legt sie fest. Der Standardwert ist „{00000000-0000-0000-0000-000000000000}“. |
| [ShowDate](../../aspose.words.drawing/signatureline/showdate/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der angibt, dass das Signaturdatum in der Signaturzeile angezeigt wird. Der Standardwert für diese Eigenschaft ist`WAHR` . |
| [Signer](../../aspose.words.drawing/signatureline/signer/) { get; set; } | Ruft den vorgeschlagenen Unterzeichner der Signaturzeile ab oder legt diesen fest. Der Standardwert für diese Eigenschaft ist**leerer String** (Empty). |
| [SignerTitle](../../aspose.words.drawing/signatureline/signertitle/) { get; set; } | Ruft den vorgeschlagenen Titel des Unterzeichners ab oder legt ihn fest (z. B. Manager). Der Standardwert für diese Eigenschaft ist**leerer String** (Empty). |

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

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
