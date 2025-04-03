---
title: PdfDigitalSignatureDetails class
linktitle: PdfDigitalSignatureDetails class
articleTitle: PdfDigitalSignatureDetails class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.PdfDigitalSignatureDetails class. Contains details for signing a PDF document with a digital signature."
type: docs
weight: 620
url: /nodejs-net/aspose.words.saving/pdfdigitalsignaturedetails/
---

## PdfDigitalSignatureDetails class

Contains details for signing a PDF document with a digital signature.


### Remarks

At the moment digitally signing PDF documents is only available on .NET 3.5 or higher.

To digitally sign a PDF document when it is created by Aspose.Words, set the [PdfSaveOptions.digitalSignatureDetails](../pdfsaveoptions/digitalSignatureDetails/) 
property to a valid [PdfDigitalSignatureDetails](./) object and then save the document in the PDF format passing 
the [PdfSaveOptions](../pdfsaveoptions/) as a parameter into the [Document.save()](../../aspose.words/document/save/#string_saveoptions) method.

Aspose.Words creates a PKCS#7 signature over the whole PDF document and uses the "Adobe.PPKMS" filter and 
"adbe.pkcs7.sha1" subfilter when creating a digital signature.




### Constructors
| Name | Description |
| --- | --- |
| [PdfDigitalSignatureDetails()](./constructor/#default) | Initializes an instance of this class. |
| [PdfDigitalSignatureDetails(certificateHolder, reason, location, signatureDate)](./constructor/#certificateholder_string_string_date) | Initializes an instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [certificateHolder](./certificateHolder/) | Returns the certificate holder object that contains the certificate was used to sign the document. |
| [hashAlgorithm](./hashAlgorithm/) | Gets or sets the hash algorithm. |
| [location](./location/) | Gets or sets the location of the signing. |
| [reason](./reason/) | Gets or sets the reason for the signing. |
| [signatureDate](./signatureDate/) | Gets or sets the date of the signing. |
| [timestampSettings](./timestampSettings/) | Gets or sets the digital signature timestamp settings. |

### Examples

Shows how to sign a generated PDF document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Contents of signed PDF.");

let certificateHolder = aw.DigitalSignatures.CertificateHolder.create(base.myDir + "morzal.pfx", "aw");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
// digitally sign the document as we render it with the "Save" method.
let signingTime = new Date(2015, 7, 20);
options.digitalSignatureDetails =
  new aw.Saving.PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.digitalSignatureDetails.hashAlgorithm = aw.Saving.PdfDigitalSignatureHashAlgorithm.RipeMD160;

expect(options.digitalSignatureDetails.reason).toEqual("Test Signing");
expect(options.digitalSignatureDetails.location).toEqual("My Office");
//expect(options.digitalSignatureDetails.signatureDate).toEqual(signingTime);

doc.save(base.artifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../)
* property [PdfSaveOptions.digitalSignatureDetails](../pdfsaveoptions/digitalSignatureDetails/)

