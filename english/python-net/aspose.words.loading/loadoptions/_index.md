---
title: LoadOptions class
linktitle: LoadOptions class
articleTitle: LoadOptions class
second_title: Aspose.Words for Python
description: "aspose.words.loading.LoadOptions class. Allows to specify additional options (such as password or base URI) when loading a document into a [Document](../../aspose.words/document/) object"
type: docs
weight: 110
url: /python-net/aspose.words.loading/loadoptions/
---

## LoadOptions class

Allows to specify additional options (such as password or base URI) when
loading a document into a [Document](../../aspose.words/document/) object.
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/python-net/specify-load-options/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [LoadOptions()](./__init__/#default) | Initializes a new instance of this class with default values. |
| [LoadOptions(password)](./__init__/#str) | A shortcut to initialize a new instance of this class with the specified password to load an encrypted document. |
| [LoadOptions(load_format, password, base_uri)](./__init__/#loadformat_str_str) | A shortcut to initialize a new instance of this class with properties set to the specified values. |

### Properties

| Name | Description |
| --- | --- |
| [base_uri](./base_uri/) | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be ``None`` or empty string. Default is ``None``. |
| [convert_metafiles_to_png](./convert_metafiles_to_png/) | Gets or sets whether to convert metafile(Wmf or Emf) images to Png image format. |
| [convert_shape_to_office_math](./convert_shape_to_office_math/) | Gets or sets whether to convert shapes with EquationXML to Office Math objects. |
| [encoding](./encoding/) | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be ``None``. Default is ``None``. |
| [font_settings](./font_settings/) | Allows to specify document font settings. |
| [ignore_ole_data](./ignore_ole_data/) | Specifies whether to ignore the OLE data. |
| [language_preferences](./language_preferences/) | Gets language preferences that will be used when document is loading. |
| [load_format](./load_format/) | Specifies the format of the document to be loaded. Default is [LoadFormat.AUTO](../../aspose.words/loadformat/#AUTO). |
| [msw_version](./msw_version/) | Allows to specify that the document loading process should match a specific MS Word version. Default value is [MsWordVersion.WORD2019](../../aspose.words.settings/mswordversion/#WORD2019) |
| [password](./password/) | Gets or sets the password for opening an encrypted document. Can be ``None`` or empty string. Default is ``None``. |
| [preserve_include_picture_field](./preserve_include_picture_field/) | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is ``False``. |
| [progress_callback](./progress_callback/) | Called during loading a document and accepts data about loading progress. |
| [resource_loading_callback](./resource_loading_callback/) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [temp_folder](./temp_folder/) | Allows to use temporary files when reading document. By default this property is ``None`` and no temporary files are used. |
| [update_dirty_fields](./update_dirty_fields/) | Specifies whether to update the fields with the ``dirty`` attribute. |
| [warning_callback](./warning_callback/) | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss. |

### Examples

Shows how to load an encrypted Microsoft Word document.

```python
# Aspose.Words throw an exception if we try to open an encrypted document without its password.
with self.assertRaises(Exception):
    doc = aw.Document(MY_DIR + "Encrypted.docx")

# When loading such a document, the password is passed to the document's constructor using a LoadOptions object.
options = aw.loading.LoadOptions("docPassword")

# There are two ways of loading an encrypted document with a LoadOptions object.
# 1 -  Load the document from the local file system by filename:
doc = aw.Document(MY_DIR + "Encrypted.docx", options)

# 2 -  Load the document from a stream:
with open(MY_DIR + "Encrypted.docx", "rb") as stream:
    doc = aw.Document(stream, options)
```

### See Also

* module [aspose.words.loading](../)

