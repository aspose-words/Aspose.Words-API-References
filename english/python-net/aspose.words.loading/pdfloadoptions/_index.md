---
title: PdfLoadOptions class
linktitle: PdfLoadOptions class
articleTitle: PdfLoadOptions class
second_title: Aspose.Words for Python
description: "aspose.words.loading.PdfLoadOptions class. Allows to specify additional options when loading Pdf document into a [Document](../../aspose.words/document/) object"
type: docs
weight: 140
url: /python-net/aspose.words.loading/pdfloadoptions/
---

## PdfLoadOptions class

Allows to specify additional options when loading Pdf document into a [Document](../../aspose.words/document/) object.
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/python-net/specify-load-options/) documentation article.




**Inheritance:** [PdfLoadOptions](./) → [LoadOptions](../loadoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [PdfLoadOptions()](./__init__/#default) | The default constructor. |

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
| [page_count](./page_count/) | Gets or sets the number of pages to read. Default is MaxValue which means all pages of the document will be read. |
| [page_index](./page_index/) | Gets or sets the 0-based index of the first page to read. Default is 0. |
| [password](../loadoptions/password/) | Gets or sets the password for opening an encrypted document. Can be ``None`` or empty string. Default is ``None``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [preserve_include_picture_field](../loadoptions/preserve_include_picture_field/) | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is ``False``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [progress_callback](../loadoptions/progress_callback/) | Called during loading a document and accepts data about loading progress.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [recovery_mode](../loadoptions/recovery_mode/) | Defines how the document should be handled if errors occur during loading.   Use this property to specify whether the system should attempt to recover the document  or follow another defined behavior.   The default value is [DocumentRecoveryMode.TRY_RECOVER](../documentrecoverymode/#TRY_RECOVER).<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [resource_loading_callback](../loadoptions/resource_loading_callback/) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [skip_pdf_images](./skip_pdf_images/) | Gets or sets the flag indicating whether images must be skipped while loading PDF document. Default is ``False``. |
| [temp_folder](../loadoptions/temp_folder/) | Allows to use temporary files when reading document. By default this property is ``None`` and no temporary files are used.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [update_dirty_fields](../loadoptions/update_dirty_fields/) | Specifies whether to update the fields with the ``dirty`` attribute.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [use_system_lcid](../loadoptions/use_system_lcid/) | Gets or sets whether to use LCID value obtained from Windows registry to determine page setup default margins.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [warning_callback](../loadoptions/warning_callback/) | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss.<br>(Inherited from [LoadOptions](../loadoptions/)) |

### Examples

Shows how to skip images during loading PDF files.

```python
options = aw.loading.PdfLoadOptions()
options.skip_pdf_images = is_skip_pdf_images
options.page_index = 0
options.page_count = 1
doc = aw.Document(file_name=MY_DIR + 'Images.pdf', load_options=options)
shape_collection = doc.get_child_nodes(aw.NodeType.SHAPE, True)
if is_skip_pdf_images:
    self.assertEqual(shape_collection.count, 0)
else:
    self.assertNotEqual(shape_collection.count, 0)
```

### See Also

* module [aspose.words.loading](../)
* class [LoadOptions](../loadoptions/)

