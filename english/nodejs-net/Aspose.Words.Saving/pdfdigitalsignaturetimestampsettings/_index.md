---
title: PdfDigitalSignatureTimestampSettings class
linktitle: PdfDigitalSignatureTimestampSettings class
articleTitle: PdfDigitalSignatureTimestampSettings class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.PdfDigitalSignatureTimestampSettings class. Contains settings of the digital signature timestamp"
type: docs
weight: 630
url: /nodejs-net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/
---

## PdfDigitalSignatureTimestampSettings class

Contains settings of the digital signature timestamp.
To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/nodejs-net/working-with-digital-signatures/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [PdfDigitalSignatureTimestampSettings()](./constructor/#default) | Initializes an instance of this class. |
| [PdfDigitalSignatureTimestampSettings(serverUrl, userName, password)](./constructor/#string_string_string) | Initializes an instance of this class. |
| [PdfDigitalSignatureTimestampSettings(serverUrl, userName, password, timeout)](./constructor/#string_string_string_unknown) | Initializes an instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [password](./password/) | Timestamp server password. |
| [serverUrl](./serverUrl/) | Timestamp server URL. |
| [timeout](./timeout/) | Time-out value for accessing timestamp server. |
| [userName](./userName/) | Timestamp server user name. |

### Examples

Shows how to sign a saved PDF document digitally and timestamp it.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Signed PDF contents.");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// Create a digital signature and assign it to our SaveOptions object to sign the document when we save it to PDF.
let certificateHolder = aw.DigitalSignatures.CertificateHolder.create(base.myDir + "morzal.pfx", "aw");
options.digitalSignatureDetails = new aw.Saving.PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", Date.now());

// Create a timestamp authority-verified timestamp.
options.digitalSignatureDetails.timestampSettings =
  new aw.Saving.PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword");

// The default lifespan of the timestamp is 100 seconds.
expect(options.digitalSignatureDetails.timestampSettings.timeout.totalSeconds).toEqual(100.0);

const timeout = {
  get minutes() { return 30; }
}

// We can set our timeout period via the constructor.
options.digitalSignatureDetails.timestampSettings =
  new aw.Saving.PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", timeout);

expect(options.digitalSignatureDetails.timestampSettings.timeout.totalSeconds).toEqual(1800);
expect(options.digitalSignatureDetails.timestampSettings.serverUrl).toEqual("https://freetsa.org/tsr");
expect(options.digitalSignatureDetails.timestampSettings.userName).toEqual("JohnDoe");
expect(options.digitalSignatureDetails.timestampSettings.password).toEqual("MyPassword");

// The "Save" method will apply our signature to the output document at this time.
doc.save(base.artifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../)

