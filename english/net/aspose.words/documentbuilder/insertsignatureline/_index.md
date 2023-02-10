---
title: DocumentBuilder.InsertSignatureLine
second_title: Aspose.Words for .NET API Reference
description: DocumentBuilder method. Inserts a signature line at the current position in C#.
type: docs
weight: 440
url: /net/aspose.words/documentbuilder/insertsignatureline/
---
## InsertSignatureLine(SignatureLineOptions) {#insertsignatureline}

Inserts a signature line at the current position.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | The object that stores parameters of creating signature line. |

### Return Value

The signature line node that was just inserted.

## Examples

Shows how to sign a document with a personal certificate and a signature line.

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

// Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
// indicating that the signature line contains a signature.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* class [SignatureLineOptions](../../signaturelineoptions/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

---

## InsertSignatureLine(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) {#insertsignatureline_1}

Inserts a signature line at the specified position.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    WrapType wrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | The object that stores parameters of creating signature line. |
| horzPos | RelativeHorizontalPosition | Specifies where the distance to the signature line is measured from. |
| left | Double | Distance in points from the origin to the left side of the signature line. |
| vertPos | RelativeVerticalPosition | Specifies where the distance to the signature line measured from. |
| top | Double | Distance in points from the origin to the top side of the signature line. |
| wrapType | WrapType | Specifies how to wrap text around the signature line. |

### Return Value

The signature line node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples

Shows how to insert an inline signature line into a document.

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

// The signature line can be signed in Microsoft Word by double clicking it.
doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineInline.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* class [SignatureLineOptions](../../signaturelineoptions/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
