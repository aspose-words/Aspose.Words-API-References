---
title: LoadOptions Class
linktitle: LoadOptions
articleTitle: LoadOptions
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.LoadOptions for enhanced document loading. Set passwords and base URIs effortlessly for seamless integration and security.
type: docs
weight: 4090
url: /net/aspose.words.loading/loadoptions/
---
## LoadOptions class

Allows to specify additional options (such as password or base URI) when loading a document into a [`Document`](../../aspose.words/document/) object.

To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/net/specify-load-options/) documentation article.

```csharp
public class LoadOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [LoadOptions](loadoptions/#constructor)() | Initializes a new instance of this class with default values. |
| [LoadOptions](loadoptions/#constructor_2)(*string*) | A shortcut to initialize a new instance of this class with the specified password to load an encrypted document. |
| [LoadOptions](loadoptions/#constructor_1)(*[LoadFormat](../../aspose.words/loadformat/), string, string*) | A shortcut to initialize a new instance of this class with properties set to the specified values. |

## Properties

| Name | Description |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be `null` or empty string. Default is `null`. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Gets or sets whether to convert metafile(Wmf or Emf) images to Png image format. |
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
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Allows to use temporary files when reading document. By default this property is `null` and no temporary files are used. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Specifies whether to update the fields with the `dirty` attribute. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Gets or sets whether to use LCID value obtained from Windows registry to determine page setup default margins. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss. |

## Methods

| Name | Description |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Determines whether the specified object is equal in value to the current object. |

## Examples

Shows how to load an encrypted Microsoft Word document.

```csharp
Document doc;

// Aspose.Words throw an exception if we try to open an encrypted document without its password.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// When loading such a document, the password is passed to the document's constructor using a LoadOptions object.
LoadOptions options = new LoadOptions("docPassword");

// There are two ways of loading an encrypted document with a LoadOptions object.
// 1 -  Load the document from the local file system by filename:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 -  Load the document from a stream:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### See Also

* namespace [Aspose.Words.Loading](../../aspose.words.loading/)
* assembly [Aspose.Words](../../)
