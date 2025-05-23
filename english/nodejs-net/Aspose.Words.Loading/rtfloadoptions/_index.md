﻿---
title: RtfLoadOptions class
linktitle: RtfLoadOptions class
articleTitle: RtfLoadOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Loading.RtfLoadOptions class. Allows to specify additional options when loading [LoadFormat.Rtf](../../aspose.words/loadformat/#Rtf) document into a [Document](../../aspose.words/document/) object"
type: docs
weight: 160
url: /nodejs-net/aspose.words.loading/rtfloadoptions/
---

## RtfLoadOptions class

Allows to specify additional options when loading [LoadFormat.Rtf](../../aspose.words/loadformat/#Rtf) document into a [Document](../../aspose.words/document/) object.
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/nodejs-net/specify-load-options/) documentation article.




**Inheritance:** [RtfLoadOptions](./) → [LoadOptions](../loadoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [RtfLoadOptions()](./constructor/#default) | Initializes a new instance of this class with default values. |

### Properties

| Name | Description |
| --- | --- |
| [baseUri](../loadoptions/baseUri/) | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be ``null`` or empty string. Default is ``null``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convertMetafilesToPng](../loadoptions/convertMetafilesToPng/) | Gets or sets whether to convert metafile(Wmf or Emf) images to Png image format.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convertShapeToOfficeMath](../loadoptions/convertShapeToOfficeMath/) | Gets or sets whether to convert shapes with EquationXML to Office Math objects.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [encoding](../loadoptions/encoding/) | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be ``null``. Default is ``null``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [fontSettings](../loadoptions/fontSettings/) | Allows to specify document font settings.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [ignoreOleData](../loadoptions/ignoreOleData/) | Specifies whether to ignore the OLE data.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [languagePreferences](../loadoptions/languagePreferences/) | Gets language preferences that will be used when document is loading.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [loadFormat](../loadoptions/loadFormat/) | Specifies the format of the document to be loaded. Default is [LoadFormat.Auto](../../aspose.words/loadformat/#Auto).<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [mswVersion](../loadoptions/mswVersion/) | Allows to specify that the document loading process should match a specific MS Word version. Default value is [MsWordVersion.Word2019](../../aspose.words.settings/mswordversion/#Word2019)<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [password](../loadoptions/password/) | Gets or sets the password for opening an encrypted document. Can be ``null`` or empty string. Default is ``null``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [preserveIncludePictureField](../loadoptions/preserveIncludePictureField/) | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is ``false``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [recognizeUtf8Text](./recognizeUtf8Text/) | When set to ``true``,  will try to detect UTF8 characters,  they will be preserved during import. |
| [resourceLoadingCallback](../loadoptions/resourceLoadingCallback/) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [tempFolder](../loadoptions/tempFolder/) | Allows to use temporary files when reading document. By default this property is ``null`` and no temporary files are used.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [updateDirtyFields](../loadoptions/updateDirtyFields/) | Specifies whether to update the fields with the ``dirty`` attribute.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [useSystemLcid](../loadoptions/useSystemLcid/) | Gets or sets whether to use LCID value obtained from Windows registry to determine page setup default margins.<br>(Inherited from [LoadOptions](../loadoptions/)) |

### Examples

Shows how to detect UTF-8 characters while loading an RTF document.

```js
// Create an "RtfLoadOptions" object to modify how we load an RTF document.
let loadOptions = new aw.Loading.RtfLoadOptions();

// Set the "RecognizeUtf8Text" property to "false" to assume that the document uses the ISO 8859-1 charset
// and loads every character in the document.
// Set the "RecognizeUtf8Text" property to "true" to parse any variable-length characters that may occur in the text.
loadOptions.recognizeUtf8Text = recognizeUtf8Text;

let doc = new aw.Document(base.myDir + "UTF-8 characters.rtf", loadOptions);

expect(doc.firstSection.body.getText().trim()).toEqual(recognizeUtf8Text
  ? "“John Doe´s list of currency symbols”™\r€, ¢, £, ¥, ¤"
  : "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\râ‚¬, Â¢, Â£, Â¥, Â¤");
```

### See Also

* module [Aspose.Words.Loading](../)
* class [LoadOptions](../loadoptions/)

