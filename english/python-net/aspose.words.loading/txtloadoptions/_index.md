---
title: TxtLoadOptions class
second_title: Aspose.Words for Python via .NET API Reference
description: "Allows to specify additional options when loading [LoadFormat.TEXT](../../aspose.words/loadformat/#TEXT) document into a [Document](../../aspose.words/document/) object"
type: docs
weight: 180
url: /python-net/aspose.words.loading/txtloadoptions/
---

## TxtLoadOptions class

Allows to specify additional options when loading [LoadFormat.TEXT](../../aspose.words/loadformat/#TEXT) document into a [Document](../../aspose.words/document/) object.
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/net/specify-load-options/) documentation article.




**Inheritance:** [TxtLoadOptions](./) → [LoadOptions](../loadoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [TxtLoadOptions()](./__init__/#default) | Initializes a new instance of this class with default values. |

### Properties

| Name | Description |
| --- | --- |
| [auto_numbering_detection](./auto_numbering_detection/) | Gets or sets a boolean value indicating either automatic numbering detection will be performed while loading a document. The default value is ``True``. |
| [base_uri](../loadoptions/base_uri/) | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be ``None`` or empty string. Default is ``None``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convert_metafiles_to_png](../loadoptions/convert_metafiles_to_png/) | Gets or sets whether to convert metafile (Aspose.FileFormat.Wmf or Aspose.FileFormat.Emf) images to Aspose.FileFormat.Png image format.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convert_shape_to_office_math](../loadoptions/convert_shape_to_office_math/) | Gets or sets whether to convert shapes with EquationXML to Office Math objects.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [detect_numbering_with_whitespaces](./detect_numbering_with_whitespaces/) | Allows to specify how numbered list items are recognized when document is imported from plain text format. The default value is ``True``. |
| [document_direction](./document_direction/) | Gets or sets a document direction. The default value is [DocumentDirection.LEFT_TO_RIGHT](../documentdirection/#LEFT_TO_RIGHT). |
| [encoding](../loadoptions/encoding/) | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be ``None``. Default is ``None``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [font_settings](../loadoptions/font_settings/) | Allows to specify document font settings.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [ignore_ole_data](../loadoptions/ignore_ole_data/) | Specifies whether to ignore the OLE data.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [language_preferences](../loadoptions/language_preferences/) | Gets language preferences that will be used when document is loading.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [leading_spaces_options](./leading_spaces_options/) | Gets or sets preferred option of a leading space handling. Default value is Aspose.Words.Loading.TxtLeadingSpacesOptions.ConvertToIndent. |
| [load_format](../loadoptions/load_format/) | Specifies the format of the document to be loaded. Default is [LoadFormat.AUTO](../../aspose.words/loadformat/#AUTO).<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [msw_version](../loadoptions/msw_version/) | Allows to specify that the document loading process should match a specific MS Word version. Default value is [MsWordVersion.WORD2019](../../aspose.words.settings/mswordversion/#WORD2019)<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [password](../loadoptions/password/) | Gets or sets the password for opening an encrypted document. Can be ``None`` or empty string. Default is ``None``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [preserve_include_picture_field](../loadoptions/preserve_include_picture_field/) | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is ``False``.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [progress_callback](../loadoptions/progress_callback/) | Called during loading a document and accepts data about loading progress.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [resource_loading_callback](../loadoptions/resource_loading_callback/) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [temp_folder](../loadoptions/temp_folder/) | Allows to use temporary files when reading document. By default this property is ``None`` and no temporary files are used.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [trailing_spaces_options](./trailing_spaces_options/) | Gets or sets preferred option of a trailing space handling. Default value is Aspose.Words.Loading.TxtTrailingSpacesOptions.Trim. |
| [update_dirty_fields](../loadoptions/update_dirty_fields/) | Specifies whether to update the fields with the ``dirty`` attribute.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [warning_callback](../loadoptions/warning_callback/) | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss.<br>(Inherited from [LoadOptions](../loadoptions/)) |

### See Also

* module [aspose.words.loading](../)
* class [LoadOptions](../loadoptions/)

