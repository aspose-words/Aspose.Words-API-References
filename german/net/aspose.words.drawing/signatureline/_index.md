---
title: SignatureLine Class
linktitle: SignatureLine
articleTitle: SignatureLine
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.SignatureLine, um Signaturzeileneigenschaften für eine verbesserte Dokumentsicherheit einfach zu verwalten und anzupassen.
type: docs
weight: 1700
url: /de/net/aspose.words.drawing/signatureline/
---
## SignatureLine class

Bietet Zugriff auf die Eigenschaften der Signaturzeile.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit digitalen Signaturen](https://docs.aspose.com/words/net/working-with-digital-signatures/) Dokumentationsartikel.

```csharp
public class SignatureLine
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowComments](../../aspose.words.drawing/signatureline/allowcomments/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, dass der Unterzeichner im Dialogfeld „Signieren“ Kommentare hinzufügen kann. Der Standardwert für diese Eigenschaft ist`FALSCH` . |
| [DefaultInstructions](../../aspose.words.drawing/signatureline/defaultinstructions/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, dass im Dialogfeld „Signieren“ Standardanweisungen angezeigt werden. Der Standardwert für diese Eigenschaft ist`WAHR` . |
| [Email](../../aspose.words.drawing/signatureline/email/) { get; set; } | Ruft die E-Mail-Adresse des vorgeschlagenen Unterzeichners ab oder legt sie fest. Der Standardwert für diese Eigenschaft ist**leere Zeichenfolge** (Empty ). |
| [Id](../../aspose.words.drawing/signatureline/id/) { get; set; } | Ruft die Kennung für diese Signaturzeile ab oder legt sie fest. |
| [Instructions](../../aspose.words.drawing/signatureline/instructions/) { get; set; } | Ruft Anweisungen für den Unterzeichner ab oder legt diese fest, die beim Unterschreiben der Signaturzeile angezeigt werden. Diese Eigenschaft wird ignoriert, wenn[`DefaultInstructions`](./defaultinstructions/) ist gesetzt. Der Standardwert für diese Eigenschaft ist**leere Zeichenfolge** (Empty ). |
| [IsSigned](../../aspose.words.drawing/signatureline/issigned/) { get; } | Gibt an, dass die Signaturzeile mit einer digitalen Signatur versehen ist. |
| [IsValid](../../aspose.words.drawing/signatureline/isvalid/) { get; } | Gibt an, dass die Signaturzeile mit einer digitalen Signatur versehen ist und diese digitale Signatur gültig ist. |
| [ProviderId](../../aspose.words.drawing/signatureline/providerid/) { get; set; } | Ruft die Signaturanbieterkennung für diese Signaturzeile ab oder legt sie fest. Der Standardwert ist "{00000000-0000-0000-0000-000000000000}". |
| [ShowDate](../../aspose.words.drawing/signatureline/showdate/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, dass das Signaturdatum in der Signaturzeile angezeigt wird. Der Standardwert für diese Eigenschaft ist`WAHR` . |
| [Signer](../../aspose.words.drawing/signatureline/signer/) { get; set; } | Ruft den vorgeschlagenen Unterzeichner der Signaturzeile ab oder legt ihn fest. Der Standardwert für diese Eigenschaft ist**leere Zeichenfolge** (Empty ). |
| [SignerTitle](../../aspose.words.drawing/signatureline/signertitle/) { get; set; } | Ruft den vorgeschlagenen Titel des Unterzeichners ab oder legt ihn fest (z. B. Manager). Der Standardwert für diese Eigenschaft ist**leere Zeichenfolge** (Empty ). |

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

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
