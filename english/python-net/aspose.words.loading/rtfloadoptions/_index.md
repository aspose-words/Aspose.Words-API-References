---
title: RtfLoadOptions class
linktitle: RtfLoadOptions class
articleTitle: RtfLoadOptions class
second_title: Aspose.Words for Python
description: "aspose.words.loading.RtfLoadOptions class. Allows to specify additional options when loading [LoadFormat.RTF](../../aspose.words/loadformat/#RTF) document into a [Document](../../aspose.words/document/) object"
type: docs
weight: 160
url: /python-net/aspose.words.loading/rtfloadoptions/
---

## RtfLoadOptions class

Allows to specify additional options when loading [LoadFormat.RTF](../../aspose.words/loadformat/#RTF) document into a [Document](../../aspose.words/document/) object.
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/python-net/specify-load-options/) documentation article.




**Inheritance:** [RtfLoadOptions](./) → [LoadOptions](../loadoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [RtfLoadOptions()](./__init__/#default) | Initializes a new instance of this class with default values. |

### Properties

| Name | Description |
| --- | --- |
| [base_uri](../loadoptions/base_uri/) | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be ``None`` or empty string. Default is ``None``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convert_metafiles_to_png](../loadoptions/convert_metafiles_to_png/) | Gets or sets whether to convert metafile (Aspose.FileFormat.Wmf or Aspose.FileFormat.Emf) images to Aspose.FileFormat.Png image format.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convert_shape_to_office_math](../loadoptions/convert_shape_to_office_math/) | Gets or sets whether to convert shapes with EquationXML to Office Math objects.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [encoding](../loadoptions/encoding/) | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be ``None``. Default is ``None``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [font_settings](../loadoptions/font_settings/) | Allows to specify document font settings.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [ignore_ole_data](../loadoptions/ignore_ole_data/) | Specifies whether to ignore the OLE data.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [language_preferences](../loadoptions/language_preferences/) | Gets language preferences that will be used when document is loading.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [load_format](../loadoptions/load_format/) | Specifies the format of the document to be loaded. Default is [LoadFormat.AUTO](../../aspose.words/loadformat/#AUTO).<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [msw_version](../loadoptions/msw_version/) | Allows to specify that the document loading process should match a specific MS Word version. Default value is [MsWordVersion.WORD2019](../../aspose.words.settings/mswordversion/#WORD2019)<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [password](../loadoptions/password/) | Gets or sets the password for opening an encrypted document. Can be ``None`` or empty string. Default is ``None``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [preserve_include_picture_field](../loadoptions/preserve_include_picture_field/) | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is ``False``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [progress_callback](../loadoptions/progress_callback/) | Called during loading a document and accepts data about loading progress.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [recognize_utf8_text](./recognize_utf8_text/) | When set to ``True``, Aspose.Charset.CharsetDetector will try to detect UTF8 characters,  they will be preserved during import. |
| [resource_loading_callback](../loadoptions/resource_loading_callback/) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [temp_folder](../loadoptions/temp_folder/) | Allows to use temporary files when reading document. By default this property is ``None`` and no temporary files are used.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [update_dirty_fields](../loadoptions/update_dirty_fields/) | Specifies whether to update the fields with the ``dirty`` attribute.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [warning_callback](../loadoptions/warning_callback/) | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss.<br>(Inherited from [LoadOptions](../loadoptions/)) |

### Examples

Shows how to detect UTF-8 characters while loading an RTF document.

```python
# Create an "RtfLoadOptions" object to modify how we load an RTF document.
load_options = aw.loading.RtfLoadOptions()

# Set the "recognize_utf8_text" property to "False" to assume that the document uses the ISO 8859-1 charset
# and loads every character in the document.
# Set the "recognize_utf8_text" property to "True" to parse any variable-length characters that may occur in the text.
load_options.recognize_utf8_text = recognize_utf8_text

doc = aw.Document(MY_DIR + "UTF-8 characters.rtf", load_options)

if recognize_utf8_text:
    self.assertEqual(
        "“John Doe´s list of currency symbols”™\r" + "€, ¢, £, ¥, ¤",
        doc.first_section.body.get_text().strip())
else:
    self.assertEqual(
        "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r" + "â‚¬, Â¢, Â£, Â¥, Â¤",
        doc.first_section.body.get_text().strip())
```

### See Also

* module [aspose.words.loading](../)
* class [LoadOptions](../loadoptions/)

