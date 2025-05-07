---
title: HtmlLoadOptions class
linktitle: HtmlLoadOptions class
articleTitle: HtmlLoadOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Loading.HtmlLoadOptions class. Allows to specify additional options when loading HTML document into a [Document](../../aspose.words/document/) object"
type: docs
weight: 70
url: /nodejs-net/aspose.words.loading/htmlloadoptions/
---

## HtmlLoadOptions class

Allows to specify additional options when loading HTML document into a [Document](../../aspose.words/document/) object.
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/nodejs-net/specify-load-options/) documentation article.




**Inheritance:** [HtmlLoadOptions](./) → [LoadOptions](../loadoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [HtmlLoadOptions()](./constructor/#default) | Initializes a new instance of this class with default values. |
| [HtmlLoadOptions(password)](./constructor/#string) | A shortcut to initialize a new instance of this class with the specified password to load an encrypted document. |
| [HtmlLoadOptions(loadFormat, password, baseUri)](./constructor/#loadformat_string_string) | A shortcut to initialize a new instance of this class with properties set to the specified values. |

### Properties

| Name | Description |
| --- | --- |
| [baseUri](../loadoptions/baseUri/) | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be ``null`` or empty string. Default is ``null``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [blockImportMode](./blockImportMode/) | Gets or sets a value that specifies how properties of block-level elements are imported. Default value is [BlockImportMode.Merge](../blockimportmode/#Merge). |
| [convertMetafilesToPng](../loadoptions/convertMetafilesToPng/) | Gets or sets whether to convert metafile(Wmf or Emf) images to Png image format.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convertShapeToOfficeMath](../loadoptions/convertShapeToOfficeMath/) | Gets or sets whether to convert shapes with EquationXML to Office Math objects.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convertSvgToEmf](./convertSvgToEmf/) | Gets or sets a value indicating whether to convert loaded SVG images to the EMF format. Default value is ``false`` and, if possible, loaded SVG images are stored as is without conversion. |
| [encoding](../loadoptions/encoding/) | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be ``null``. Default is ``null``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [fontSettings](../loadoptions/fontSettings/) | Allows to specify document font settings.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [ignoreNoscriptElements](./ignoreNoscriptElements/) | Gets or sets a value indicating whether to ignore \<noscript\> HTML elements. Default value is ``false``. |
| [ignoreOleData](../loadoptions/ignoreOleData/) | Specifies whether to ignore the OLE data.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [languagePreferences](../loadoptions/languagePreferences/) | Gets language preferences that will be used when document is loading.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [loadFormat](../loadoptions/loadFormat/) | Specifies the format of the document to be loaded. Default is [LoadFormat.Auto](../../aspose.words/loadformat/#Auto).<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [mswVersion](../loadoptions/mswVersion/) | Allows to specify that the document loading process should match a specific MS Word version. Default value is [MsWordVersion.Word2019](../../aspose.words.settings/mswordversion/#Word2019)<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [password](../loadoptions/password/) | Gets or sets the password for opening an encrypted document. Can be ``null`` or empty string. Default is ``null``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [preferredControlType](./preferredControlType/) | Gets or sets preferred type of document nodes that will represent imported \<input\> and \<select\> elements. Default value is [HtmlControlType.FormField](../htmlcontroltype/#FormField). |
| [preserveIncludePictureField](../loadoptions/preserveIncludePictureField/) | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is ``false``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [resourceLoadingCallback](../loadoptions/resourceLoadingCallback/) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [supportFontFaceRules](./supportFontFaceRules/) | Gets or sets a value indicating whether to support @font-face rules and whether to load declared fonts. Default value is ``false``. |
| [supportVml](./supportVml/) | Gets or sets a value indicating whether to support VML images. |
| [tempFolder](../loadoptions/tempFolder/) | Allows to use temporary files when reading document. By default this property is ``null`` and no temporary files are used.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [updateDirtyFields](../loadoptions/updateDirtyFields/) | Specifies whether to update the fields with the ``dirty`` attribute.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [useSystemLcid](../loadoptions/useSystemLcid/) | Gets or sets whether to use LCID value obtained from Windows registry to determine page setup default margins.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [webRequestTimeout](./webRequestTimeout/) | The number of milliseconds to wait before the web request times out. The default value is 100000 milliseconds (100 seconds). |

### Examples

Shows how to support conditional comments while loading an HTML document.

```js
let loadOptions = new aw.Loading.HtmlLoadOptions();

// If the value is true, then we take VML code into account while parsing the loaded document.
loadOptions.supportVml = supportVml;

// This document contains a JPEG image within "<!--[if gte vml 1]>" tags,
// and a different PNG image within "<![if !vml]>" tags.
// If we set the "SupportVml" flag to "true", then Aspose.words will load the JPEG.
// If we set this flag to "false", then Aspose.words will only load the PNG.
let doc = new aw.Document(base.myDir + "VML conditional.htm", loadOptions);

if (supportVml)
  expect(doc.getShape(0, true).imageData.imageType).toEqual(aw.Drawing.ImageType.Jpeg);
else
  expect(doc.getShape(0, true).imageData.imageType).toEqual(aw.Drawing.ImageType.Png);
```

### See Also

* module [Aspose.Words.Loading](../)
* class [LoadOptions](../loadoptions/)

