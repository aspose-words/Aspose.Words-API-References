---
title: PdfLoadOptions class
second_title: Aspose.Words for Python via .NET API Reference
description: "Allows to specify additional options when loading Pdf document into a [Document](../../aspose.words/document/) object."
type: docs
weight: 120
url: /python-net/aspose.words.loading/pdfloadoptions/
---

## PdfLoadOptions class

Allows to specify additional options when loading Pdf document into a [Document](../../aspose.words/document/) object.



**Inheritance:** [PdfLoadOptions](./) → [LoadOptions](../loadoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [PdfLoadOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [base_uri](../loadoptions/base_uri/) | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be null or empty string. Default is null.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convert_metafiles_to_png](../loadoptions/convert_metafiles_to_png/) | Gets or sets whether to convert metafile (Aspose.FileFormat.Wmf or Aspose.FileFormat.Emf) images to Aspose.FileFormat.Png image format.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [convert_shape_to_office_math](../loadoptions/convert_shape_to_office_math/) | Gets or sets whether to convert shapes with EquationXML to Office Math objects.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [encoding](../loadoptions/encoding/) | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be null. Default is null.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [flat_opc_xml_mapping_only](../loadoptions/flat_opc_xml_mapping_only/) | Gets or sets value determining which document formats are allowed to be mapped by [StructuredDocumentTag.xml_mapping](../../aspose.words.markup/structureddocumenttag/xml_mapping/). By default only [LoadFormat.FLAT_OPC](../../aspose.words/loadformat/#FLAT_OPC) document format is allowed to be mapped.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [font_settings](../loadoptions/font_settings/) | Allows to specify document font settings.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [language_preferences](../loadoptions/language_preferences/) | Gets language preferences that will be used when document is loading.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [load_format](../loadoptions/load_format/) | Specifies the format of the document to be loaded. Default is [LoadFormat.AUTO](../../aspose.words/loadformat/#AUTO).<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [msw_version](../loadoptions/msw_version/) | Allows to specify that the document loading process should match a specific MS Word version. Default value is [MsWordVersion.WORD2019](../../aspose.words.settings/mswordversion/#WORD2019)<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [page_count](./page_count/) | Gets or sets the number of pages to read. Default is MaxValue which means all pages of the document will be read. |
| [page_index](./page_index/) | Gets or sets the 0-based index of the first page to read. Default is 0. |
| [password](../loadoptions/password/) | Gets or sets the password for opening an encrypted document. Can be null or empty string. Default is null.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [preserve_include_picture_field](../loadoptions/preserve_include_picture_field/) | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is false.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [progress_callback](../loadoptions/progress_callback/) | Called during loading a document and accepts data about loading progress.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [resource_loading_callback](../loadoptions/resource_loading_callback/) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [skip_pdf_images](./skip_pdf_images/) | Gets or sets the flag indicating whether images must be skipped while loading PDF document. Default is False. |
| [temp_folder](../loadoptions/temp_folder/) | Allows to use temporary files when reading document. By default this property is ``null`` and no temporary files are used.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [update_dirty_fields](../loadoptions/update_dirty_fields/) | Specifies whether to update the fields with the ``dirty`` attribute.<br>(Inherited from [LoadOptions](../loadoptions/)) |
| [warning_callback](../loadoptions/warning_callback/) | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss.<br>(Inherited from [LoadOptions](../loadoptions/)) |

### See Also

* module [aspose.words.loading](../)
* class [LoadOptions](../loadoptions/)

