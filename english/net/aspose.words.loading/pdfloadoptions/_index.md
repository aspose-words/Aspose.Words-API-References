---
title: PdfLoadOptions Class
linktitle: PdfLoadOptions
articleTitle: PdfLoadOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Loading.PdfLoadOptions class. Allows to specify additional options when loading Pdf document into a Document object in C#.
type: docs
weight: 4090
url: /net/aspose.words.loading/pdfloadoptions/
---
## PdfLoadOptions class

Allows to specify additional options when loading Pdf document into a [`Document`](../../aspose.words/document/) object.

To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/net/specify-load-options/) documentation article.

```csharp
public class PdfLoadOptions : LoadOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [PdfLoadOptions](pdfloadoptions/)() | The default constructor. |

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
| [PageCount](../../aspose.words.loading/pdfloadoptions/pagecount/) { get; set; } | Gets or sets the number of pages to read. Default is MaxValue which means all pages of the document will be read. |
| [PageIndex](../../aspose.words.loading/pdfloadoptions/pageindex/) { get; set; } | Gets or sets the 0-based index of the first page to read. Default is 0. |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Gets or sets the password for opening an encrypted document. Can be `null` or empty string. Default is `null`. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is `false`. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Called during loading a document and accepts data about loading progress. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [SkipPdfImages](../../aspose.words.loading/pdfloadoptions/skippdfimages/) { get; set; } | Gets or sets the flag indicating whether images must be skipped while loading PDF document. Default is `false`. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Allows to use temporary files when reading document. By default this property is `null` and no temporary files are used. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Specifies whether to update the fields with the `dirty` attribute. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Gets or sets whether to use LCID value obtained from Windows registry to determine page setup default margins. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss. |

## Methods

| Name | Description |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Determines whether the specified object is equal in value to the current object. |

## Examples

Shows how to skip images during loading PDF files.

```csharp
PdfLoadOptions options = new PdfLoadOptions();
options.SkipPdfImages = isSkipPdfImages;
options.PageIndex = 0;
options.PageCount = 1;

Document doc = new Document(MyDir + "Images.pdf", options);
NodeCollection shapeCollection = doc.GetChildNodes(NodeType.Shape, true);

if (isSkipPdfImages)
    Assert.AreEqual(shapeCollection.Count, 0);
else
    Assert.AreNotEqual(shapeCollection.Count, 0);
```

### See Also

* class [LoadOptions](../loadoptions/)
* namespace [Aspose.Words.Loading](../../aspose.words.loading/)
* assembly [Aspose.Words](../../)
