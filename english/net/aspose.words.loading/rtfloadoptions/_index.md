---
title: RtfLoadOptions Class
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Loading.RtfLoadOptions class. Allows to specify additional options when loading Rtf document into a Document object in C#.
type: docs
weight: 3530
url: /net/aspose.words.loading/rtfloadoptions/
---
## RtfLoadOptions class

Allows to specify additional options when loading Rtf document into a [`Document`](../../aspose.words/document/) object.

To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/net/specify-load-options/) documentation article.

```csharp
public class RtfLoadOptions : LoadOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [RtfLoadOptions](rtfloadoptions/)() | Initializes a new instance of this class with default values. |

## Properties

| Name | Description |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be `null` or empty string. Default is `null`. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Gets or sets whether to convert metafile (Wmf or Emf) images to Png image format. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Gets or sets whether to convert shapes with EquationXML to Office Math objects. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be `null`. Default is `null`. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Allows to specify document font settings. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Specifies whether to ignore the OLE data. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Gets language preferences that will be used when document is loading. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Specifies the format of the document to be loaded. Default is Auto. |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Allows to specify that the document loading process should match a specific MS Word version. Default value is Word2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Gets or sets the password for opening an encrypted document. Can be `null` or empty string. Default is `null`. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is `false`. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Called during loading a document and accepts data about loading progress. |
| [RecognizeUtf8Text](../../aspose.words.loading/rtfloadoptions/recognizeutf8text/) { get; set; } | When set to `true`, CharsetDetector will try to detect UTF8 characters, they will be preserved during import. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Allows to use temporary files when reading document. By default this property is `null` and no temporary files are used. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Specifies whether to update the fields with the `dirty` attribute. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss. |

## Examples

Shows how to detect UTF-8 characters while loading an RTF document.

```csharp
// Create an "RtfLoadOptions" object to modify how we load an RTF document.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Set the "RecognizeUtf8Text" property to "false" to assume that the document uses the ISO 8859-1 charset
// and loads every character in the document.
// Set the "RecognizeUtf8Text" property to "true" to parse any variable-length characters that may occur in the text.
loadOptions.RecognizeUtf8Text = recognizeUtf8Text;

Document doc = new Document(MyDir + "UTF-8 characters.rtf", loadOptions);

Assert.AreEqual(
    recognizeUtf8Text
        ? "“John Doe´s list of currency symbols”™\r" +
          "€, ¢, £, ¥, ¤"
        : "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r" +
          "â‚¬, Â¢, Â£, Â¥, Â¤",
    doc.FirstSection.Body.GetText().Trim());
```

### See Also

* class [LoadOptions](../loadoptions/)
* namespace [Aspose.Words.Loading](../../aspose.words.loading/)
* assembly [Aspose.Words](../../)
