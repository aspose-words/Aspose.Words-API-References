---
title: ChmLoadOptions Class
linktitle: ChmLoadOptions
articleTitle: ChmLoadOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Loading.ChmLoadOptions class. Allows to specify additional options when loading CHM document into a Document object in C#.
type: docs
weight: 3820
url: /net/aspose.words.loading/chmloadoptions/
---
## ChmLoadOptions class

Allows to specify additional options when loading CHM document into a [`Document`](../../aspose.words/document/) object.

To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/net/specify-load-options/) documentation article.

```csharp
public class ChmLoadOptions : LoadOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [ChmLoadOptions](chmloadoptions/)() | Initializes a new instance of this class with default values. |

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
| [OriginalFileName](../../aspose.words.loading/chmloadoptions/originalfilename/) { get; set; } | The name of the CHM file. Default value is `null`. |
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

Shows how to resolve URLs like "ms-its:myfile.chm::/index.htm".

```csharp
// Our document contains URLs like "ms-its:amhelp.chm::....htm", but it has a different name,
// so file links don't work after saving it to HTML.
// We need to define the original filename in 'ChmLoadOptions' to avoid this behavior.
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### See Also

* class [LoadOptions](../loadoptions/)
* namespace [Aspose.Words.Loading](../../aspose.words.loading/)
* assembly [Aspose.Words](../../)
