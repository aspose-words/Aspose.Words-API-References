---
title: InsertSignatureLine
second_title: Aspose.Words für .NET-API-Referenz
description: Fügt eine Signaturzeile an der aktuellen Position ein.
type: docs
weight: 420
url: /de/net/aspose.words/documentbuilder/insertsignatureline/
---
## InsertSignatureLine(SignatureLineOptions) {#insertsignatureline}

Fügt eine Signaturzeile an der aktuellen Position ein.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | Das Objekt, das Parameter zum Erstellen einer Signaturzeile speichert. |

### Rückgabewert

Der soeben eingefügte Signaturzeilenknoten.

### Beispiele

Zeigt, wie ein Dokument mit einem persönlichen Zertifikat und einer Signaturzeile signiert wird.

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

// Öffnen Sie unser gespeichertes Dokument erneut und überprüfen Sie, ob die Eigenschaften "IsSigned" und "IsValid" beide gleich "true" sind,
// zeigt an, dass die Signaturzeile eine Signatur enthält.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape)
* class [SignatureLineOptions](../../signaturelineoptions)
* class [DocumentBuilder](../../documentbuilder)
* namensraum [Aspose.Words](../../documentbuilder)
* Montage [Aspose.Words](../../../)

---

## InsertSignatureLine(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) {#insertsignatureline_1}

Fügt eine Signaturzeile an der angegebenen Position ein.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    WrapType wrapType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | Das Objekt, das Parameter zum Erstellen einer Signaturzeile speichert. |
| horzPos | RelativeHorizontalPosition | Gibt an, von wo aus der Abstand zur Signaturlinie gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite der Signaturlinie. |
| vertPos | RelativeVerticalPosition | Gibt an, von wo aus der Abstand zur Signaturlinie gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung bis zur Oberseite der Signaturlinie. |
| wrapType | WrapType | Gibt an, wie Text um die Signaturzeile herum umbrochen wird. |

### Rückgabewert

Der soeben eingefügte Signaturzeilenknoten.

### Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape) Objekt, das von dieser Methode zurückgegeben wird.

### Beispiele

Zeigt, wie Sie eine Inline-Signaturzeile in ein Dokument einfügen.

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

// Die Signaturzeile kann in Microsoft Word per Doppelklick signiert werden.
doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineInline.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape)
* class [SignatureLineOptions](../../signaturelineoptions)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition)
* enum [WrapType](../../../aspose.words.drawing/wraptype)
* class [DocumentBuilder](../../documentbuilder)
* namensraum [Aspose.Words](../../documentbuilder)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
