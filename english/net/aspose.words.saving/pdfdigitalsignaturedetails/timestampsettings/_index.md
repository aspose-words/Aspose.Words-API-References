---
title: PdfDigitalSignatureDetails.TimestampSettings
linktitle: TimestampSettings
second_title: Aspose.Words for .NET API Reference
description: PdfDigitalSignatureDetails TimestampSettings property. Gets or sets the digital signature timestamp settings in C#.
type: docs
weight: 70
url: /net/aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/
---
## TimestampSettings property

Gets or sets the digital signature timestamp settings.

```csharp
public PdfDigitalSignatureTimestampSettings TimestampSettings { get; set; }
```

## Remarks

The default value is `null` and the digital signature will not be time-stamped. When this property is set to a valid [`PdfDigitalSignatureTimestampSettings`](../../pdfdigitalsignaturetimestampsettings/) object, then the digital signature in the PDF document will be time-stamped.

## Examples

Shows how to sign a saved PDF document digitally and timestamp it.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Create a digital signature and assign it to our SaveOptions object to sign the document when we save it to PDF. 
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Create a timestamp authority-verified timestamp.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// The default lifespan of the timestamp is 100 seconds.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// We can set our timeout period via the constructor.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// The "Save" method will apply our signature to the output document at this time.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### See Also

* class [PdfDigitalSignatureTimestampSettings](../../pdfdigitalsignaturetimestampsettings/)
* class [PdfDigitalSignatureDetails](../)
* namespace [Aspose.Words.Saving](../../pdfdigitalsignaturedetails/)
* assembly [Aspose.Words](../../../)
