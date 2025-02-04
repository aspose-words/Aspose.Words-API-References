---
title: PdfDigitalSignatureTimestampSettings Class
linktitle: PdfDigitalSignatureTimestampSettings
articleTitle: PdfDigitalSignatureTimestampSettings
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.PdfDigitalSignatureTimestampSettings class. Contains settings of the digital signature timestamp in C#.
type: docs
weight: 6080
url: /net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/
---
## PdfDigitalSignatureTimestampSettings class

Contains settings of the digital signature timestamp.

To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/net/working-with-digital-signatures/) documentation article.

```csharp
public class PdfDigitalSignatureTimestampSettings
```

## Constructors

| Name | Description |
| --- | --- |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor)() | Initializes an instance of this class. |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor_1)(*string, string, string*) | Initializes an instance of this class. |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor_2)(*string, string, string, TimeSpan*) | Initializes an instance of this class. |

## Properties

| Name | Description |
| --- | --- |
| [Password](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/password/) { get; set; } | Timestamp server password. |
| [ServerUrl](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/serverurl/) { get; set; } | Timestamp server URL. |
| [Timeout](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/timeout/) { get; set; } | Time-out value for accessing timestamp server. |
| [UserName](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/username/) { get; set; } | Timestamp server user name. |

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

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
