---
title: MarkdownLoadOptions class
linktitle: MarkdownLoadOptions class
articleTitle: MarkdownLoadOptions class
second_title: Aspose.Words for Python
description: "aspose.words.loading.MarkdownLoadOptions class. Allows to specify additional options when loading [LoadFormat.MARKDOWN](../../aspose.words/loadformat/#MARKDOWN) document into a [Document](../../aspose.words/document/) object."
type: docs
weight: 120
url: /python-net/aspose.words.loading/markdownloadoptions/
---

## MarkdownLoadOptions class

Allows to specify additional options when loading [LoadFormat.MARKDOWN](../../aspose.words/loadformat/#MARKDOWN) document into a [Document](../../aspose.words/document/) object.



**Inheritance:** [MarkdownLoadOptions](./) → [LoadOptions](../loadoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [MarkdownLoadOptions()](./__init__/#default) | Initializes a new instance of [MarkdownLoadOptions](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [base_uri](../loadoptions/base_uri/) | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be ``None`` or empty string. Default is ``None``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convert_metafiles_to_png](../loadoptions/convert_metafiles_to_png/) | Gets or sets whether to convert metafile(Wmf or Emf) images to Png image format.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convert_shape_to_office_math](../loadoptions/convert_shape_to_office_math/) | Gets or sets whether to convert shapes with EquationXML to Office Math objects.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [encoding](../loadoptions/encoding/) | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be ``None``. Default is ``None``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [font_settings](../loadoptions/font_settings/) | Allows to specify document font settings.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [ignore_ole_data](../loadoptions/ignore_ole_data/) | Specifies whether to ignore the OLE data.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [language_preferences](../loadoptions/language_preferences/) | Gets language preferences that will be used when document is loading.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [load_format](../loadoptions/load_format/) | Specifies the format of the document to be loaded. Default is [LoadFormat.AUTO](../../aspose.words/loadformat/#AUTO).<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [msw_version](../loadoptions/msw_version/) | Allows to specify that the document loading process should match a specific MS Word version. Default value is [MsWordVersion.WORD2019](../../aspose.words.settings/mswordversion/#WORD2019)<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [password](../loadoptions/password/) | Gets or sets the password for opening an encrypted document. Can be ``None`` or empty string. Default is ``None``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [preserve_empty_lines](./preserve_empty_lines/) | Gets or sets a boolean value indicating whether to preserve empty lines while load a [LoadFormat.MARKDOWN](../../aspose.words/loadformat/#MARKDOWN) document. The default value is ``False``. Normally, empty lines between block-level elements in Markdown are ignored. Empty lines at the beginning and end of the document are also ignored. This option allows to import such empty lines. |
| [preserve_include_picture_field](../loadoptions/preserve_include_picture_field/) | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is ``False``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [progress_callback](../loadoptions/progress_callback/) | Called during loading a document and accepts data about loading progress.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [resource_loading_callback](../loadoptions/resource_loading_callback/) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [temp_folder](../loadoptions/temp_folder/) | Allows to use temporary files when reading document. By default this property is ``None`` and no temporary files are used.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [update_dirty_fields](../loadoptions/update_dirty_fields/) | Specifies whether to update the fields with the ``dirty`` attribute.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [warning_callback](../loadoptions/warning_callback/) | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss.<br>(Inherited from [LoadOptions](../loadoptions/)) |

### Examples

Shows how to preserve empty line while load a document.

```python
md_text = f"{os.linesep}Line1{os.linesep}{os.linesep}Line2{os.linesep}{os.linesep}"
stream = io.BytesIO(str.encode(md_text))
stream.seek(0)

load_options = aw.loading.MarkdownLoadOptions()
load_options.preserve_empty_lines = True
doc = aw.Document(stream, load_options)

self.assertEqual("\rLine1\r\rLine2\r\f", doc.get_text())
```

### See Also

* module [aspose.words.loading](../)
* class [LoadOptions](../loadoptions/)

