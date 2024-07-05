---
title: PdfEncryptionDetails
linktitle: PdfEncryptionDetails
articleTitle: PdfEncryptionDetails
second_title: Aspose.Words for .NET
description: PdfEncryptionDetails constructor. Initializes an instance of this class in C#.
type: docs
weight: 10
url: /net/aspose.words.saving/pdfencryptiondetails/pdfencryptiondetails/
---
## PdfEncryptionDetails(*string, string*) {#constructor}

Initializes an instance of this class.

```csharp
public PdfEncryptionDetails(string userPassword, string ownerPassword)
```

## Examples

Shows how to load encrypted pdf using plugin.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world! This is an encrypted PDF document.");

// Configure a SaveOptions object to encrypt this PDF document while saving it to the local file system.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("MyPassword", string.Empty);

Assert.AreEqual(PdfPermissions.DisallowAll, encryptionDetails.Permissions);

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.EncryptionDetails = encryptionDetails;

doc.Save(ArtifactsDir + "PDF2Word.LoadEncryptedPdfUsingPlugin.pdf", saveOptions);

Document pdfDoc = new Document();

// To load a password encrypted document, we need to pass a LoadOptions object
// with the correct password stored in its "Password" property.
LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

Aspose.Words.Pdf2Word.PdfDocumentReaderPlugin pdf2Word = new Aspose.Words.Pdf2Word.PdfDocumentReaderPlugin();
using (FileStream stream =
    new FileStream(ArtifactsDir + "PDF2Word.LoadEncryptedPdfUsingPlugin.pdf", FileMode.Open))
{
    // Pass the LoadOptions object into the Pdf2Word plugin's "Read" method
    // the same way we would pass it into a document's "Load" method.
    pdf2Word.Read(stream, new LoadOptions("MyPassword"), pdfDoc);
}

Assert.AreEqual("Hello world! This is an encrypted PDF document.",
    pdfDoc.GetText().Trim());
```

### See Also

* class [PdfEncryptionDetails](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)

---

## PdfEncryptionDetails(*string, string, [PdfPermissions](../../pdfpermissions/)*) {#constructor_1}

Initializes an instance of this class.

```csharp
public PdfEncryptionDetails(string userPassword, string ownerPassword, PdfPermissions permissions)
```

## Examples

Shows how to set permissions on a saved PDF document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Extend permissions to allow the editing of annotations.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Enable encryption via the "EncryptionDetails" property.
saveOptions.EncryptionDetails = encryptionDetails;

// When we open this document, we will need to provide the password before accessing its contents.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### See Also

* enum [PdfPermissions](../../pdfpermissions/)
* class [PdfEncryptionDetails](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
