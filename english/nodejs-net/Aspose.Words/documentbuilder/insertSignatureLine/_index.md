---
title: DocumentBuilder.insertSignatureLine method
linktitle: insertSignatureLine method
articleTitle: insertSignatureLine method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DocumentBuilder.insertSignatureLine method"
type: docs
weight: 470
url: /nodejs-net/aspose.words/documentbuilder/insertSignatureLine/
---

## insertSignatureLine(signatureLineOptions) {#signaturelineoptions}

Inserts a signature line at the current position.


```js
insertSignatureLine(signatureLineOptions: Aspose.Words.SignatureLineOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../signaturelineoptions/) | The object that stores parameters of creating signature line. |

### Returns

The signature line node that was just inserted.


## insertSignatureLine(signatureLineOptions, horzPos, left, vertPos, top, wrapType) {#signaturelineoptions_relativehorizontalposition_number_relativeverticalposition_number_wraptype}

Inserts a signature line at the specified position.


```js
insertSignatureLine(signatureLineOptions: Aspose.Words.SignatureLineOptions, horzPos: Aspose.Words.Drawing.RelativeHorizontalPosition, left: number, vertPos: Aspose.Words.Drawing.RelativeVerticalPosition, top: number, wrapType: Aspose.Words.Drawing.WrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../signaturelineoptions/) | The object that stores parameters of creating signature line. |
| horzPos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) | Specifies where the distance to the signature line is measured from. |
| left | number | Distance in points from the origin to the left side of the signature line. |
| vertPos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) | Specifies where the distance to the signature line measured from. |
| top | number | Distance in points from the origin to the top side of the signature line. |
| wrapType | [WrapType](../../../aspose.words.drawing/wraptype/) | Specifies how to wrap text around the signature line. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The signature line node that was just inserted.


## Examples

Shows how to sign a document with a personal certificate and a signature line.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let signatureLineOptions = new aw.SignatureLineOptions
{
  Signer = "vderyushev",
  SignerTitle = "QA",
  Email = "vderyushev@aspose.com",
  ShowDate = true,
  DefaultInstructions = false,
  Instructions = "Please sign here.",
  AllowComments = true
};

let signatureLine = builder.insertSignatureLine(signatureLineOptions).SignatureLine;
signatureLine.providerId = Guid.parse("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2");

expect(signatureLine.isSigned).toEqual(false);
expect(signatureLine.isValid).toEqual(false);

doc.save(base.artifactsDir + "DocumentBuilder.SignatureLineProviderId.docx");

let signOptions = new aw.DigitalSignatures.SignOptions
{
  SignatureLineId = signatureLine.id,
  ProviderId = signatureLine.providerId,
  Comments = "Document was signed by vderyushev",
  SignTime = Date.now()
};

let certHolder = aw.DigitalSignatures.CertificateHolder.create(base.myDir + "morzal.pfx", "aw");

aw.DigitalSignatures.DigitalSignatureUtil.sign(base.artifactsDir + "DocumentBuilder.SignatureLineProviderId.docx", 
  base.artifactsDir + "DocumentBuilder.SignatureLineProviderId.signed.docx", certHolder, signOptions);

// Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
// indicating that the signature line contains a signature.
doc = new aw.Document(base.artifactsDir + "DocumentBuilder.SignatureLineProviderId.signed.docx");
let shape = (Shape)doc.getShape(0, true);
signatureLine = shape.signatureLine;

expect(signatureLine.isSigned).toEqual(true);
expect(signatureLine.isValid).toEqual(true);
```

Shows how to insert an inline signature line into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let options = new aw.SignatureLineOptions();
options.signer = "John Doe",
options.signerTitle = "Manager",
options.email = "johndoe@aspose.com",
options.showDate = true,
options.defaultInstructions = false,
options.instructions = "Please sign here.",
options.allowComments = true

builder.insertSignatureLine(options, aw.Drawing.RelativeHorizontalPosition.RightMargin, 2.0,
  aw.Drawing.RelativeVerticalPosition.Page, 3.0, aw.Drawing.WrapType.Inline);

// The signature line can be signed in Microsoft Word by double clicking it.
doc.save(base.artifactsDir + "DocumentBuilder.SignatureLineInline.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

