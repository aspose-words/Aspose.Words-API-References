---
title: HtmlLoadOptions Class
linktitle: HtmlLoadOptions
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Loading.HtmlLoadOptions class. Allows to specify additional options when loading HTML document into a Document object in C#.
type: docs
weight: 3480
url: /net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

Allows to specify additional options when loading HTML document into a [`Document`](../../aspose.words/document/) object.

To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/net/specify-load-options/) documentation article.

```csharp
public class HtmlLoadOptions : LoadOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | Initializes a new instance of this class with default values. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(*string*) | A shortcut to initialize a new instance of this class with the specified password to load an encrypted document. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(*[LoadFormat](../../aspose.words/loadformat/), string, string*) | A shortcut to initialize a new instance of this class with properties set to the specified values. |

## Properties

| Name | Description |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be `null` or empty string. Default is `null`. |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | Gets or sets a value that specifies how properties of block-level elements are imported. Default value is Merge. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Gets or sets whether to convert metafile (Wmf or Emf) images to Png image format. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Gets or sets whether to convert shapes with EquationXML to Office Math objects. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | Gets or sets a value indicating whether to convert loaded SVG images to the EMF format. Default value is `false` and, if possible, loaded SVG images are stored as is without conversion. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be `null`. Default is `null`. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Allows to specify document font settings. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | Gets or sets a value indicating whether to ignore &lt;noscript&gt; HTML elements. Default value is `false`. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Specifies whether to ignore the OLE data. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Gets language preferences that will be used when document is loading. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Specifies the format of the document to be loaded. Default is Auto. |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Allows to specify that the document loading process should match a specific MS Word version. Default value is Word2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Gets or sets the password for opening an encrypted document. Can be `null` or empty string. Default is `null`. |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | Gets or sets preferred type of document nodes that will represent imported &lt;input&gt; and &lt;select&gt; elements. Default value is FormField. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is `false`. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Called during loading a document and accepts data about loading progress. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | Gets or sets a value indicating whether to support VML images. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Allows to use temporary files when reading document. By default this property is `null` and no temporary files are used. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Specifies whether to update the fields with the `dirty` attribute. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | The number of milliseconds to wait before the web request times out. The default value is 100000 milliseconds (100 seconds). |

### See Also

* class [LoadOptions](../loadoptions/)
* namespace [Aspose.Words.Loading](../../aspose.words.loading/)
* assembly [Aspose.Words](../../)
