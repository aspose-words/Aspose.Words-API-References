﻿---
title: ChmLoadOptions class
linktitle: ChmLoadOptions class
articleTitle: ChmLoadOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Loading.ChmLoadOptions class. Allows to specify additional options when loading CHM document into a [Document](../../aspose.words/document/) object"
type: docs
weight: 20
url: /nodejs-net/aspose.words.loading/chmloadoptions/
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
| [baseUri](../loadoptions/baseUri/) | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be ``null`` or empty string. Default is ``null``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convertMetafilesToPng](../loadoptions/convertMetafilesToPng/) | Gets or sets whether to convert metafile(Wmf or Emf) images to Png image format.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convertShapeToOfficeMath](../loadoptions/convertShapeToOfficeMath/) | Gets or sets whether to convert shapes with EquationXML to Office Math objects.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [encoding](../loadoptions/encoding/) | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be ``null``. Default is ``null``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [fontSettings](../loadoptions/fontSettings/) | Allows to specify document font settings.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [ignoreOleData](../loadoptions/ignoreOleData/) | Specifies whether to ignore the OLE data.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [languagePreferences](../loadoptions/languagePreferences/) | Gets language preferences that will be used when document is loading.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [loadFormat](../loadoptions/loadFormat/) | Specifies the format of the document to be loaded. Default is [LoadFormat.Auto](../../aspose.words/loadformat/#Auto).<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [mswVersion](../loadoptions/mswVersion/) | Allows to specify that the document loading process should match a specific MS Word version. Default value is [MsWordVersion.Word2019](../../aspose.words.settings/mswordversion/#Word2019)<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [originalFileName](./originalFileName/) | The name of the CHM file. Default value is ``null``. |
| [password](../loadoptions/password/) | Gets or sets the password for opening an encrypted document. Can be ``null`` or empty string. Default is ``null``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [preserveIncludePictureField](../loadoptions/preserveIncludePictureField/) | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is ``false``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [recoveryMode](../loadoptions/recoveryMode/) | Defines how the document should be handled if errors occur during loading.   Use this property to specify whether the system should attempt to recover the document  or follow another defined behavior.   The default value is [DocumentRecoveryMode.TryRecover](../documentrecoverymode/#TryRecover).<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [resourceLoadingCallback](../loadoptions/resourceLoadingCallback/) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [tempFolder](../loadoptions/tempFolder/) | Allows to use temporary files when reading document. By default this property is ``null`` and no temporary files are used.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [updateDirtyFields](../loadoptions/updateDirtyFields/) | Specifies whether to update the fields with the ``dirty`` attribute.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [useSystemLcid](../loadoptions/useSystemLcid/) | Gets or sets whether to use LCID value obtained from Windows registry to determine page setup default margins.<br>(Inherited from [LoadOptions](../loadoptions/)) |

### Examples

Shows how to resolve URLs like "ms-its:myfile.chm::/index.htm".

```js
// Our document contains URLs like "ms-its:amhelp.chm::....htm", but it has a different name,
// so file links don't work after saving it to HTML.
// We need to define the original filename in 'ChmLoadOptions' to avoid this behavior.
let loadOptions = new aw.Loading.ChmLoadOptions();
loadOptions.originalFileName = "amhelp.chm";

let doc = new aw.Document(base.myDir + "Document with ms-its links.chm", loadOptions);

doc.save(base.artifactsDir + "ExChmLoadOptions.originalFileName.html");
```

### See Also

* module [Aspose.Words.Loading](../)
* class [LoadOptions](../loadoptions/)

