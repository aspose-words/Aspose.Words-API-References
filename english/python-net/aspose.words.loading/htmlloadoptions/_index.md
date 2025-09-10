---
title: HtmlLoadOptions class
linktitle: HtmlLoadOptions class
articleTitle: HtmlLoadOptions class
second_title: Aspose.Words for Python
description: "aspose.words.loading.HtmlLoadOptions class. Allows to specify additional options when loading HTML document into a [Document](../../aspose.words/document/) object"
type: docs
weight: 80
url: /python-net/aspose.words.loading/htmlloadoptions/
---

## HtmlLoadOptions class

Allows to specify additional options when loading HTML document into a [Document](../../aspose.words/document/) object.
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/python-net/specify-load-options/) documentation article.




**Inheritance:** [HtmlLoadOptions](./) → [LoadOptions](../loadoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [HtmlLoadOptions()](./__init__/#default) | Initializes a new instance of this class with default values. |
| [HtmlLoadOptions(password)](./__init__/#str) | A shortcut to initialize a new instance of this class with the specified password to load an encrypted document. |
| [HtmlLoadOptions(load_format, password, base_uri)](./__init__/#loadformat_str_str) | A shortcut to initialize a new instance of this class with properties set to the specified values. |

### Properties

| Name | Description |
| --- | --- |
| [base_uri](../loadoptions/base_uri/) | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be ``None`` or empty string. Default is ``None``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [block_import_mode](./block_import_mode/) | Gets or sets a value that specifies how properties of block-level elements are imported. Default value is [BlockImportMode.MERGE](../blockimportmode/#MERGE). |
| [convert_metafiles_to_png](../loadoptions/convert_metafiles_to_png/) | Gets or sets whether to convert metafile(Wmf or Emf) images to Png image format.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convert_shape_to_office_math](../loadoptions/convert_shape_to_office_math/) | Gets or sets whether to convert shapes with EquationXML to Office Math objects.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convert_svg_to_emf](./convert_svg_to_emf/) | Gets or sets a value indicating whether to convert loaded SVG images to the EMF format. Default value is ``False`` and, if possible, loaded SVG images are stored as is without conversion. |
| [encoding](../loadoptions/encoding/) | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be ``None``. Default is ``None``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [font_settings](../loadoptions/font_settings/) | Allows to specify document font settings.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [ignore_noscript_elements](./ignore_noscript_elements/) | Gets or sets a value indicating whether to ignore \<noscript\> HTML elements. Default value is ``False``. |
| [ignore_ole_data](../loadoptions/ignore_ole_data/) | Specifies whether to ignore the OLE data.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [language_preferences](../loadoptions/language_preferences/) | Gets language preferences that will be used when document is loading.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [load_format](../loadoptions/load_format/) | Specifies the format of the document to be loaded. Default is [LoadFormat.AUTO](../../aspose.words/loadformat/#AUTO).<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [msw_version](../loadoptions/msw_version/) | Allows to specify that the document loading process should match a specific MS Word version. Default value is [MsWordVersion.WORD2019](../../aspose.words.settings/mswordversion/#WORD2019)<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [password](../loadoptions/password/) | Gets or sets the password for opening an encrypted document. Can be ``None`` or empty string. Default is ``None``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [preferred_control_type](./preferred_control_type/) | Gets or sets preferred type of document nodes that will represent imported \<input\> and \<select\> elements. Default value is [HtmlControlType.FORM_FIELD](../htmlcontroltype/#FORM_FIELD). |
| [preserve_include_picture_field](../loadoptions/preserve_include_picture_field/) | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is ``False``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [progress_callback](../loadoptions/progress_callback/) | Called during loading a document and accepts data about loading progress.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [recovery_mode](../loadoptions/recovery_mode/) | Defines how the document should be handled if errors occur during loading.   Use this property to specify whether the system should attempt to recover the document  or follow another defined behavior.   The default value is [DocumentRecoveryMode.TRY_RECOVER](../documentrecoverymode/#TRY_RECOVER).<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [resource_loading_callback](../loadoptions/resource_loading_callback/) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [support_font_face_rules](./support_font_face_rules/) | Gets or sets a value indicating whether to support @font-face rules and whether to load declared fonts. Default value is ``False``. |
| [support_vml](./support_vml/) | Gets or sets a value indicating whether to support VML images. |
| [temp_folder](../loadoptions/temp_folder/) | Allows to use temporary files when reading document. By default this property is ``None`` and no temporary files are used.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [update_dirty_fields](../loadoptions/update_dirty_fields/) | Specifies whether to update the fields with the ``dirty`` attribute.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [use_system_lcid](../loadoptions/use_system_lcid/) | Gets or sets whether to use LCID value obtained from Windows registry to determine page setup default margins.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [warning_callback](../loadoptions/warning_callback/) | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [web_request_timeout](./web_request_timeout/) | The number of milliseconds to wait before the web request times out. The default value is 100000 milliseconds (100 seconds). |

### Examples

Shows how to support conditional comments while loading an HTML document.

```python
load_options = aw.loading.HtmlLoadOptions()
# If the value is true, then we take VML code into account while parsing the loaded document.
load_options.support_vml = support_vml
# This document contains a JPEG image within "<!--[if gte vml 1]>" tags,
# and a different PNG image within "<![if !vml]>" tags.
# If we set the "SupportVml" flag to "true", then Aspose.Words will load the JPEG.
# If we set this flag to "false", then Aspose.Words will only load the PNG.
doc = aw.Document(file_name=MY_DIR + 'VML conditional.htm', load_options=load_options)
if support_vml:
    self.assertEqual(aw.drawing.ImageType.JPEG, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().image_data.image_type)
else:
    self.assertEqual(aw.drawing.ImageType.PNG, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().image_data.image_type)
```

### See Also

* module [aspose.words.loading](../)
* class [LoadOptions](../loadoptions/)

