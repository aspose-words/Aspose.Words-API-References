﻿---
title: ChmLoadOptions class
linktitle: ChmLoadOptions class
articleTitle: ChmLoadOptions class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Loading.ChmLoadOptions class. Allows to specify additional options when loading CHM document into a [Document](../../aspose.words/document/) object"
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Loading/chmloadoptions/
---

## ChmLoadOptions class

Allows to specify additional options when loading CHM document into a [Document](../../aspose.words/document/) object.
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/nodejs-net/specify-load-options/) documentation article.




**Inheritance:** [ChmLoadOptions](./) → [LoadOptions](../loadoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [ChmLoadOptions()](./constructor/#default) | Initializes a new instance of this class with default values. |

### Properties

| Name | Description |
| --- | --- |
| [baseUri](../loadoptions/baseUri/) | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be ``None`` or empty string. Default is ``None``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convertMetafilesToPng](../loadoptions/convertMetafilesToPng/) | Gets or sets whether to convert metafile(Wmf or Emf) images to Png image format.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convertShapeToOfficeMath](../loadoptions/convertShapeToOfficeMath/) | Gets or sets whether to convert shapes with EquationXML to Office Math objects.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [encoding](../loadoptions/encoding/) | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be ``None``. Default is ``None``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [fontSettings](../loadoptions/fontSettings/) | Allows to specify document font settings.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [ignoreOleData](../loadoptions/ignoreOleData/) | Specifies whether to ignore the OLE data.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [languagePreferences](../loadoptions/languagePreferences/) | Gets language preferences that will be used when document is loading.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [loadFormat](../loadoptions/loadFormat/) | Specifies the format of the document to be loaded. Default is [LoadFormat.Auto](../../aspose.words/loadformat/#Auto).<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [mswVersion](../loadoptions/mswVersion/) | Allows to specify that the document loading process should match a specific MS Word version. Default value is [MsWordVersion.Word2019](../../aspose.words.settings/mswordversion/#Word2019)<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [originalFileName](./originalFileName/) | The name of the CHM file. Default value is ``None``. |
| [password](../loadoptions/password/) | Gets or sets the password for opening an encrypted document. Can be ``None`` or empty string. Default is ``None``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [preserveIncludePictureField](../loadoptions/preserveIncludePictureField/) | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is ``False``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [progressCallback](../loadoptions/progressCallback/) | Called during loading a document and accepts data about loading progress.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [resourceLoadingCallback](../loadoptions/resourceLoadingCallback/) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [tempFolder](../loadoptions/tempFolder/) | Allows to use temporary files when reading document. By default this property is ``None`` and no temporary files are used.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [updateDirtyFields](../loadoptions/updateDirtyFields/) | Specifies whether to update the fields with the ``dirty`` attribute.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [useSystemLcid](../loadoptions/useSystemLcid/) | Gets or sets whether to use LCID value obtained from Windows registry to determine page setup default margins.<br>(Inherited from [LoadOptions](../loadoptions/)) |

### See Also

* module [Aspose.Words.Loading](../)
* class [LoadOptions](../loadoptions/)

