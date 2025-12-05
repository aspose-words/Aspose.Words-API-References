---
title: LoadOptions class
linktitle: LoadOptions class
articleTitle: LoadOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Loading.LoadOptions class. Allows to specify additional options (such as password or base URI) when loading a document into a [Document](../../aspose.words/document/) object"
type: docs
weight: 110
url: /nodejs-net/aspose.words.loading/loadoptions/
---

## LoadOptions class

Allows to specify additional options (such as password or base URI) when
loading a document into a [Document](../../aspose.words/document/) object.
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/nodejs-net/specify-load-options/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [LoadOptions()](./constructor/#default) | Initializes a new instance of this class with default values. |
| [LoadOptions(password)](./constructor/#string) | A shortcut to initialize a new instance of this class with the specified password to load an encrypted document. |
| [LoadOptions(loadFormat, password, baseUri)](./constructor/#loadformat_string_string) | A shortcut to initialize a new instance of this class with properties set to the specified values. |

### Properties

| Name | Description |
| --- | --- |
| [baseUri](./baseUri/) | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be ``null`` or empty string. Default is ``null``. |
| [convertMetafilesToPng](./convertMetafilesToPng/) | Gets or sets whether to convert metafile(Wmf or Emf) images to Png image format. |
| [convertShapeToOfficeMath](./convertShapeToOfficeMath/) | Gets or sets whether to convert shapes with EquationXML to Office Math objects. |
| [encoding](./encoding/) | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be ``null``. Default is ``null``. |
| [fontSettings](./fontSettings/) | Allows to specify document font settings. |
| [ignoreOleData](./ignoreOleData/) | Specifies whether to ignore the OLE data. |
| [languagePreferences](./languagePreferences/) | Gets language preferences that will be used when document is loading. |
| [loadFormat](./loadFormat/) | Specifies the format of the document to be loaded. Default is [LoadFormat.Auto](../../aspose.words/loadformat/#Auto). |
| [mswVersion](./mswVersion/) | Allows to specify that the document loading process should match a specific MS Word version. Default value is [MsWordVersion.Word2019](../../aspose.words.settings/mswordversion/#Word2019) |
| [password](./password/) | Gets or sets the password for opening an encrypted document. Can be ``null`` or empty string. Default is ``null``. |
| [preserveIncludePictureField](./preserveIncludePictureField/) | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is ``false``. |
| [recoveryMode](./recoveryMode/) | Defines how the document should be handled if errors occur during loading. Use this property to specify whether the system should attempt to recover the document or follow another defined behavior. The default value is [DocumentRecoveryMode.TryRecover](../documentrecoverymode/#TryRecover). |
| [resourceLoadingCallback](./resourceLoadingCallback/) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [tempFolder](./tempFolder/) | Allows to use temporary files when reading document. By default this property is ``null`` and no temporary files are used. |
| [updateDirtyFields](./updateDirtyFields/) | Specifies whether to update the fields with the ``dirty`` attribute. |
| [useSystemLcid](./useSystemLcid/) | Gets or sets whether to use LCID value obtained from Windows registry to determine page setup default margins. |

### Examples

Shows how to load an encrypted Microsoft Word document.

```js
// Aspose.Words throw an exception if we try to open an encrypted document without its password.
expect(() => new aw.Document(base.myDir + "Encrypted.docx")).toThrow("The document password is incorrect.");

// When loading such a document, the password is passed to the document's constructor using a LoadOptions object.
const options = new aw.Loading.LoadOptions("docPassword");

// There are two ways of loading an encrypted document with a LoadOptions object.
// 1 -  Load the document from the local file system by filename:
const doc = new aw.Document(base.myDir + "Encrypted.docx", options);

// 2 -  Load the document from a stream:
const stream = base.loadFileToBuffer(base.myDir + "Encrypted.docx");
const doc2 = new aw.Document(stream, options);
```

### See Also

* module [Aspose.Words.Loading](../)

