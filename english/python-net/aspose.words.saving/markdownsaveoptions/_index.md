﻿---
title: MarkdownSaveOptions class
linktitle: MarkdownSaveOptions class
articleTitle: MarkdownSaveOptions class
second_title: Aspose.Words for Python
description: "aspose.words.saving.MarkdownSaveOptions class. Class to specify additional options when saving a document into the [SaveFormat.MARKDOWN](../../aspose.words/saveformat/#MARKDOWN) format"
type: docs
weight: 470
url: /python-net/aspose.words.saving/markdownsaveoptions/
---

## MarkdownSaveOptions class

Class to specify additional options when saving a document into the [SaveFormat.MARKDOWN](../../aspose.words/saveformat/#MARKDOWN) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/python-net/specify-save-options/) documentation article.




**Inheritance:** [MarkdownSaveOptions](./) → [TxtSaveOptionsBase](../txtsaveoptionsbase/) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [MarkdownSaveOptions()](./__init__/#default) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.MARKDOWN](../../aspose.words/saveformat/#MARKDOWN) format. |

### Properties

| Name | Description |
| --- | --- |
| [allow_embedding_post_script_fonts](../saveoptions/allow_embedding_post_script_fonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [default_template](../saveoptions/default_template/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_3d_effects_rendering_mode](../saveoptions/dml_3d_effects_rendering_mode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_effects_rendering_mode](../saveoptions/dml_effects_rendering_mode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_rendering_mode](../saveoptions/dml_rendering_mode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [empty_paragraph_export_mode](./empty_paragraph_export_mode/) | Specifies how to export empty paragraphs to Markdown. Default value is [MarkdownEmptyParagraphExportMode.EMPTY_LINE](../markdownemptyparagraphexportmode/#EMPTY_LINE). |
| [encoding](../txtsaveoptionsbase/encoding/) | Specifies the encoding to use when exporting in text formats.  Default value is **Encoding.UTF8**.<br>(Inherited from [TxtSaveOptionsBase](../txtsaveoptionsbase/)) |
| [export_as_html](./export_as_html/) | Allows to specify the elements to be exported to Markdown as raw HTML. Default value is [MarkdownExportAsHtml.NONE](../markdownexportashtml/#NONE). |
| [export_generator_name](../saveoptions/export_generator_name/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [export_headers_footers_mode](../txtsaveoptionsbase/export_headers_footers_mode/) | Specifies the way headers and footers are exported to the text formats. Default value is [TxtExportHeadersFootersMode.PRIMARY_ONLY](../txtexportheadersfootersmode/#PRIMARY_ONLY).<br>(Inherited from [TxtSaveOptionsBase](../txtsaveoptionsbase/)) |
| [export_images_as_base64](./export_images_as_base64/) | Specifies whether images are saved in Base64 format to the output file. Default value is ``False``. |
| [export_underline_formatting](./export_underline_formatting/) | Gets or sets a boolean value indicating either to export underline text formatting as sequence of two plus characters "++". The default value is ``False``. |
| [force_page_breaks](../txtsaveoptionsbase/force_page_breaks/) | Allows to specify whether the page breaks should be preserved during export.<br>(Inherited from [TxtSaveOptionsBase](../txtsaveoptionsbase/)) |
| [image_resolution](./image_resolution/) | Specifies the output resolution for images when exporting to Markdown. Default is ``96 dpi``. |
| [image_saving_callback](./image_saving_callback/) | Allows to control how images are saved when a document is saved to [SaveFormat.MARKDOWN](../../aspose.words/saveformat/#MARKDOWN) format. |
| [images_folder](./images_folder/) | Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.MARKDOWN](../../aspose.words/saveformat/#MARKDOWN) format. Default is an empty string. |
| [images_folder_alias](./images_folder_alias/) | Specifies the name of the folder used to construct image URIs written into a document. Default is an empty string. |
| [iml_rendering_mode](../saveoptions/iml_rendering_mode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [link_export_mode](./link_export_mode/) | Specifies how links will be written to the output file. Default value is [MarkdownLinkExportMode.AUTO](../markdownlinkexportmode/#AUTO). |
| [list_export_mode](./list_export_mode/) | Specifies how list items will be written to the output file. Default value is [MarkdownListExportMode.MARKDOWN_SYNTAX](../markdownlistexportmode/#MARKDOWN_SYNTAX). |
| [memory_optimization](../saveoptions/memory_optimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [office_math_export_mode](./office_math_export_mode/) | Specifies how OfficeMath will be written to the output file. Default value is [MarkdownOfficeMathExportMode.TEXT](../markdownofficemathexportmode/#TEXT). |
| [paragraph_break](../txtsaveoptionsbase/paragraph_break/) | Specifies the string to use as a paragraph break when exporting in text formats.<br>(Inherited from [TxtSaveOptionsBase](../txtsaveoptionsbase/)) |
| [pretty_format](../saveoptions/pretty_format/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progress_callback](../saveoptions/progress_callback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [save_format](./save_format/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.MARKDOWN](../../aspose.words/saveformat/#MARKDOWN). |
| [table_content_alignment](./table_content_alignment/) | Gets or sets a value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../aspose.words/saveformat/#MARKDOWN) format. The default value is [TableContentAlignment.AUTO](../tablecontentalignment/#AUTO). |
| [temp_folder](../saveoptions/temp_folder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``None`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_ambiguous_text_font](../saveoptions/update_ambiguous_text_font/) | Determines whether the font attributes will be changed according to the character code being used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_created_time_property](../saveoptions/update_created_time_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.created_time](../../aspose.words.properties/builtindocumentproperties/created_time/) property is updated before saving. Default value is ``False``;<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_fields](../saveoptions/update_fields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_last_printed_property](../saveoptions/update_last_printed_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.last_printed](../../aspose.words.properties/builtindocumentproperties/last_printed/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_last_saved_time_property](../saveoptions/update_last_saved_time_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.last_saved_time](../../aspose.words.properties/builtindocumentproperties/last_saved_time/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [use_anti_aliasing](../saveoptions/use_anti_aliasing/) | Gets or sets a value determining whether or not to use anti-aliasing for rendering.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [use_high_quality_rendering](../saveoptions/use_high_quality_rendering/) | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Methods

| Name | Description |
| --- | --- |
|[ create_save_options(save_format)](../saveoptions/create_save_options/#saveformat) | Creates a save options object of a class suitable for the specified save format.<br>(Inherited from [SaveOptions](../saveoptions/)) |
|[ create_save_options(file_name)](../saveoptions/create_save_options/#str) | Creates a save options object of a class suitable for the file extension specified in the given file name.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### See Also

* module [aspose.words.saving](../)
* class [TxtSaveOptionsBase](../txtsaveoptionsbase/)

