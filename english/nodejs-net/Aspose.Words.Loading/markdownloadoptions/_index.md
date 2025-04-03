---
title: MarkdownLoadOptions class
linktitle: MarkdownLoadOptions class
articleTitle: MarkdownLoadOptions class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Loading.MarkdownLoadOptions class. Allows to specify additional options when loading [LoadFormat.Markdown](../../aspose.words/loadformat/#Markdown) document into a [Document](../../aspose.words/document/) object."
type: docs
weight: 120
url: /nodejs-net/aspose.words.loading/markdownloadoptions/
---

## MarkdownLoadOptions class

Allows to specify additional options when loading [LoadFormat.Markdown](../../aspose.words/loadformat/#Markdown) document into a [Document](../../aspose.words/document/) object.



**Inheritance:** [MarkdownLoadOptions](./) → [LoadOptions](../loadoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [MarkdownLoadOptions()](./constructor/#default) | Initializes a new instance of [MarkdownLoadOptions](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [baseUri](../loadoptions/baseUri/) | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be ``null`` or empty string. Default is ``null``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convertMetafilesToPng](../loadoptions/convertMetafilesToPng/) | Gets or sets whether to convert metafile(Wmf or Emf) images to Png image format.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convertShapeToOfficeMath](../loadoptions/convertShapeToOfficeMath/) | Gets or sets whether to convert shapes with EquationXML to Office Math objects.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [encoding](../loadoptions/encoding/) | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be ``null``. Default is ``null``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [fontSettings](../loadoptions/fontSettings/) | Allows to specify document font settings.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [ignoreOleData](../loadoptions/ignoreOleData/) | Specifies whether to ignore the OLE data.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [importUnderlineFormatting](./importUnderlineFormatting/) | Gets or sets a boolean value indicating either to recognize a sequence of two plus characters "++" as underline text formatting. The default value is ``false``. |
| [languagePreferences](../loadoptions/languagePreferences/) | Gets language preferences that will be used when document is loading.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [loadFormat](../loadoptions/loadFormat/) | Specifies the format of the document to be loaded. Default is [LoadFormat.Auto](../../aspose.words/loadformat/#Auto).<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [mswVersion](../loadoptions/mswVersion/) | Allows to specify that the document loading process should match a specific MS Word version. Default value is [MsWordVersion.Word2019](../../aspose.words.settings/mswordversion/#Word2019)<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [password](../loadoptions/password/) | Gets or sets the password for opening an encrypted document. Can be ``null`` or empty string. Default is ``null``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [preserveEmptyLines](./preserveEmptyLines/) | Gets or sets a boolean value indicating whether to preserve empty lines while load a [LoadFormat.Markdown](../../aspose.words/loadformat/#Markdown) document. The default value is ``false``. Normally, empty lines between block-level elements in Markdown are ignored. Empty lines at the beginning and end of the document are also ignored. This option allows to import such empty lines. |
| [preserveIncludePictureField](../loadoptions/preserveIncludePictureField/) | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is ``false``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [progressCallback](../loadoptions/progressCallback/) | Called during loading a document and accepts data about loading progress.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [resourceLoadingCallback](../loadoptions/resourceLoadingCallback/) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [tempFolder](../loadoptions/tempFolder/) | Allows to use temporary files when reading document. By default this property is ``null`` and no temporary files are used.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [updateDirtyFields](../loadoptions/updateDirtyFields/) | Specifies whether to update the fields with the ``dirty`` attribute.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [useSystemLcid](../loadoptions/useSystemLcid/) | Gets or sets whether to use LCID value obtained from Windows registry to determine page setup default margins.<br>(Inherited from [LoadOptions](../loadoptions/)) |

### Examples

Shows how to preserve empty line while load a document.

```js
string mdText = `${Environment.NewLine}Line1${Environment.NewLine}${Environment.NewLine}Line2${Environment.NewLine}${Environment.NewLine}`;
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
  let loadOptions = new aw.Loading.MarkdownLoadOptions() { PreserveEmptyLines = true };
  let doc = new aw.Document(stream, loadOptions);

  expect(doc.getText()).toEqual("\rLine1\r\rLine2\r\f");
}
```

### See Also

* module [Aspose.Words.Loading](../)
* class [LoadOptions](../loadoptions/)

