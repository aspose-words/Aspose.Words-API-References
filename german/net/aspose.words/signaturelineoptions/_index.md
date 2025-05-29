---
title: SignatureLineOptions Class
linktitle: SignatureLineOptions
articleTitle: SignatureLineOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.SignatureLineOptions, um Signaturzeilen in Ihren Dokumenten einfach anzupassen. Verbessern Sie Ihr DocumentBuilder-Erlebnis noch heute!
type: docs
weight: 6940
url: /de/net/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class

Ermöglicht die Angabe von Optionen für die einzufügende Signaturzeile. Wird verwendet in[`DocumentBuilder`](../documentbuilder/) .

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit digitalen Signaturen](https://docs.aspose.com/words/net/working-with-digital-signatures/) Dokumentationsartikel.

```csharp
public class SignatureLineOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [SignatureLineOptions](signaturelineoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowComments](../../aspose.words/signaturelineoptions/allowcomments/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, dass der Unterzeichner im Dialogfeld „Signieren“ Kommentare hinzufügen kann. Der Standardwert für diese Eigenschaft ist`FALSCH` . |
| [DefaultInstructions](../../aspose.words/signaturelineoptions/defaultinstructions/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, dass im Dialogfeld „Signieren“ Standardanweisungen angezeigt werden. Der Standardwert für diese Eigenschaft ist`WAHR` . |
| [Email](../../aspose.words/signaturelineoptions/email/) { get; set; } | Ruft die E-Mail-Adresse des vorgeschlagenen Unterzeichners ab oder legt sie fest. Der Standardwert für diese Eigenschaft ist**leere Zeichenfolge** (Empty ). |
| [Instructions](../../aspose.words/signaturelineoptions/instructions/) { get; set; } | Ruft Anweisungen für den Unterzeichner ab oder legt diese fest, die beim Unterschreiben der Signaturzeile angezeigt werden. Der Standardwert für diese Eigenschaft ist**leere Zeichenfolge** (Empty ). |
| [ShowDate](../../aspose.words/signaturelineoptions/showdate/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, dass das Signaturdatum in der Signaturzeile angezeigt wird. Der Standardwert für diese Eigenschaft ist`WAHR` . |
| [Signer](../../aspose.words/signaturelineoptions/signer/) { get; set; } | Ruft den vorgeschlagenen Unterzeichner der Signaturzeile ab oder legt ihn fest. Der Standardwert für diese Eigenschaft ist**leere Zeichenfolge** (Empty ). |
| [SignerTitle](../../aspose.words/signaturelineoptions/signertitle/) { get; set; } | Ruft den vorgeschlagenen Titel des Unterzeichners ab oder legt ihn fest. Der Standardwert für diese Eigenschaft ist**leere Zeichenfolge** (Empty ). |

## Beispiele

Zeigt, wie man ein Dokument mit einem persönlichen Zertifikat und einer Signaturzeile signiert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions signatureLineOptions = new SignatureLineOptions
{
    Signer = "vderyushev",
    SignerTitle = "QA",
    Email = "vderyushev@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
signatureLine.ProviderId = Guid.Parse("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2");

Assert.False(signatureLine.IsSigned);
Assert.False(signatureLine.IsValid);

doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx");

SignOptions signOptions = new SignOptions
{
    SignatureLineId = signatureLine.Id,
    ProviderId = signatureLine.ProviderId,
    Comments = "Document was signed by vderyushev",
    SignTime = DateTime.Now
};

CertificateHolder certHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

DigitalSignatureUtil.Sign(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx", 
    ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// Öffnen Sie unser gespeichertes Dokument erneut und überprüfen Sie, ob die Eigenschaften „IsSigned“ und „IsValid“ beide den Wert „true“ haben.
// zeigt an, dass die Signaturzeile eine Signatur enthält.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
