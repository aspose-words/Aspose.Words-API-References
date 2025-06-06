﻿---
title: TxtLoadOptions class
linktitle: TxtLoadOptions class
articleTitle: TxtLoadOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Loading.TxtLoadOptions class. Allows to specify additional options when loading [LoadFormat.Text](../../aspose.words/loadformat/#Text) document into a [Document](../../aspose.words/document/) object"
type: docs
weight: 180
url: /nodejs-net/aspose.words.loading/txtloadoptions/
---

## TxtLoadOptions class

Allows to specify additional options when loading [LoadFormat.Text](../../aspose.words/loadformat/#Text) document into a [Document](../../aspose.words/document/) object.
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/nodejs-net/specify-load-options/) documentation article.




**Inheritance:** [TxtLoadOptions](./) → [LoadOptions](../loadoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [TxtLoadOptions()](./constructor/#default) | Initializes a new instance of this class with default values. |

### Properties

| Name | Description |
| --- | --- |
| [autoNumberingDetection](./autoNumberingDetection/) | Gets or sets a boolean value indicating either automatic numbering detection will be performed while loading a document. The default value is ``true``. |
| [baseUri](../loadoptions/baseUri/) | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be ``null`` or empty string. Default is ``null``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convertMetafilesToPng](../loadoptions/convertMetafilesToPng/) | Gets or sets whether to convert metafile(Wmf or Emf) images to Png image format.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convertShapeToOfficeMath](../loadoptions/convertShapeToOfficeMath/) | Gets or sets whether to convert shapes with EquationXML to Office Math objects.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [detectHyperlinks](./detectHyperlinks/) | Specifies either to detect hyperlinks in text. The default value is ``false``. |
| [detectNumberingWithWhitespaces](./detectNumberingWithWhitespaces/) | Allows to specify how numbered list items are recognized when document is imported from plain text format. The default value is ``true``. |
| [documentDirection](./documentDirection/) | Gets or sets a document direction. The default value is [DocumentDirection.LeftToRight](../documentdirection/#LeftToRight). |
| [encoding](../loadoptions/encoding/) | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be ``null``. Default is ``null``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [fontSettings](../loadoptions/fontSettings/) | Allows to specify document font settings.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [ignoreOleData](../loadoptions/ignoreOleData/) | Specifies whether to ignore the OLE data.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [languagePreferences](../loadoptions/languagePreferences/) | Gets language preferences that will be used when document is loading.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [leadingSpacesOptions](./leadingSpacesOptions/) | Gets or sets preferred option of a leading space handling. Default value is [TxtLeadingSpacesOptions.ConvertToIndent](../txtleadingspacesoptions/#ConvertToIndent). |
| [loadFormat](../loadoptions/loadFormat/) | Specifies the format of the document to be loaded. Default is [LoadFormat.Auto](../../aspose.words/loadformat/#Auto).<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [mswVersion](../loadoptions/mswVersion/) | Allows to specify that the document loading process should match a specific MS Word version. Default value is [MsWordVersion.Word2019](../../aspose.words.settings/mswordversion/#Word2019)<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [password](../loadoptions/password/) | Gets or sets the password for opening an encrypted document. Can be ``null`` or empty string. Default is ``null``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [preserveIncludePictureField](../loadoptions/preserveIncludePictureField/) | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is ``false``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [resourceLoadingCallback](../loadoptions/resourceLoadingCallback/) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [tempFolder](../loadoptions/tempFolder/) | Allows to use temporary files when reading document. By default this property is ``null`` and no temporary files are used.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [trailingSpacesOptions](./trailingSpacesOptions/) | Gets or sets preferred option of a trailing space handling. Default value is [TxtTrailingSpacesOptions.Trim](../txttrailingspacesoptions/#Trim). |
| [updateDirtyFields](../loadoptions/updateDirtyFields/) | Specifies whether to update the fields with the ``dirty`` attribute.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [useSystemLcid](../loadoptions/useSystemLcid/) | Gets or sets whether to use LCID value obtained from Windows registry to determine page setup default margins.<br>(Inherited from [LoadOptions](../loadoptions/)) |

### Examples

Shows how to read and display hyperlinks.

```js
const inputText = "Some links in TXT:\n" +
    "https://www.aspose.com/\n" +
    "https://docs.aspose.com/words/net/\n";

// Load document with hyperlinks.
let loadOptions = new aw.Loading.TxtLoadOptions();
loadOptions.detectHyperlinks = true;
let doc = new aw.Document(Buffer.from(inputText), loadOptions);

// Print hyperlinks text.
for (let field of doc.range.fields)
  console.log(field.result);

expect(doc.range.fields.at(0).result.trim()).toEqual("https://www.aspose.com/");
expect(doc.range.fields.at(1).result.trim()).toEqual("https://docs.aspose.com/words/net/");
```

### See Also

* module [Aspose.Words.Loading](../)
* class [LoadOptions](../loadoptions/)

