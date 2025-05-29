---
title: DocumentBuilder.InsertSignatureLine
linktitle: InsertSignatureLine
articleTitle: InsertSignatureLine
second_title: Aspose.Words für .NET
description: Fügen Sie Ihren Dokumenten mühelos professionelle Signaturzeilen mit der DocumentBuilder InsertSignatureLine-Methode hinzu. Optimieren Sie Ihren Workflow noch heute!
type: docs
weight: 470
url: /de/net/aspose.words/documentbuilder/insertsignatureline/
---
## InsertSignatureLine(*[SignatureLineOptions](../../signaturelineoptions/)*) {#insertsignatureline}

Fügt an der aktuellen Position eine Signaturzeile ein.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | Das Objekt, das die Parameter zum Erstellen der Signaturzeile speichert. |

### Rückgabewert

Der gerade eingefügte Signaturzeilenknoten.

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

* class [Shape](../../../aspose.words.drawing/shape/)
* class [SignatureLineOptions](../../signaturelineoptions/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertSignatureLine(*[SignatureLineOptions](../../signaturelineoptions/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertsignatureline_1}

Fügt an der angegebenen Position eine Signaturzeile ein.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    WrapType wrapType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | Das Objekt, das die Parameter zum Erstellen der Signaturzeile speichert. |
| horzPos | RelativeHorizontalPosition | Gibt an, von wo aus der Abstand zur Signaturzeile gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite der Signaturzeile. |
| vertPos | RelativeVerticalPosition | Gibt an, von wo aus der Abstand zur Signaturzeile gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung zur Oberseite der Signaturzeile. |
| wrapType | WrapType | Gibt an, wie der Text um die Signaturzeile umbrochen wird. |

### Rückgabewert

Der gerade eingefügte Signaturzeilenknoten.

## Bemerkungen

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie eine Inline-Signaturzeile in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions options = new SignatureLineOptions
{
    Signer = "John Doe",
    SignerTitle = "Manager",
    Email = "johndoe@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, 2.0,
    RelativeVerticalPosition.Page, 3.0, WrapType.Inline);

// Die Signaturzeile kann in Microsoft Word durch Doppelklick unterschrieben werden.
doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineInline.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [SignatureLineOptions](../../signaturelineoptions/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
