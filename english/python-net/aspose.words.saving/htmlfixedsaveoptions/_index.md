﻿---
title: HtmlFixedSaveOptions class
linktitle: HtmlFixedSaveOptions class
articleTitle: HtmlFixedSaveOptions class
second_title: Aspose.Words for Python
description: "aspose.words.saving.HtmlFixedSaveOptions class. Can be used to specify additional options when saving a document into the [SaveFormat.HTML_FIXED](../../aspose.words/saveformat/#HTML_FIXED) format"
type: docs
weight: 230
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/
---

## HtmlFixedSaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.HTML_FIXED](../../aspose.words/saveformat/#HTML_FIXED) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/python-net/specify-save-options/) documentation article.




**Inheritance:** [HtmlFixedSaveOptions](./) → [FixedPageSaveOptions](../fixedpagesaveoptions/) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [HtmlFixedSaveOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [allow_embedding_post_script_fonts](../saveoptions/allow_embedding_post_script_fonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [color_mode](../fixedpagesaveoptions/color_mode/) | Gets or sets a value determining how colors are rendered.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [css_class_names_prefix](./css_class_names_prefix/) | Specifies prefix which is added to all class names in style.css file. Default value is ``"aw"``. |
| [default_template](../saveoptions/default_template/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** (System.String.Empty).<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_3d_effects_rendering_mode](../saveoptions/dml_3d_effects_rendering_mode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_effects_rendering_mode](../saveoptions/dml_effects_rendering_mode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_rendering_mode](../saveoptions/dml_rendering_mode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [encoding](./encoding/) | Specifies the encoding to use when exporting to HTML. Default value is ``new UTF8Encoding(true)`` (UTF-8 with BOM). |
| [export_embedded_css](./export_embedded_css/) | Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document. |
| [export_embedded_fonts](./export_embedded_fonts/) | Specifies whether fonts should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file. |
| [export_embedded_images](./export_embedded_images/) | Specifies whether images should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file. |
| [export_embedded_svg](./export_embedded_svg/) | Specifies whether SVG resources should be embedded into Html document. Default value is ``True``. |
| [export_form_fields](./export_form_fields/) | Gets or sets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics. |
| [export_generator_name](../saveoptions/export_generator_name/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [font_format](./font_format/) | Gets or sets [ExportFontFormat](../exportfontformat/) used for font exporting. Default value is [ExportFontFormat.WOFF](../exportfontformat/#WOFF). |
| [iml_rendering_mode](../saveoptions/iml_rendering_mode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [jpeg_quality](../fixedpagesaveoptions/jpeg_quality/) | Gets or sets a value determining the quality of the JPEG images inside Html document.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [memory_optimization](../saveoptions/memory_optimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [metafile_rendering_options](../fixedpagesaveoptions/metafile_rendering_options/) | Allows to specify metafile rendering options.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [numeral_format](../fixedpagesaveoptions/numeral_format/) | Gets or sets [NumeralFormat](../numeralformat/) used for rendering of numerals. European numerals are used by default.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [optimize_output](./optimize_output/) | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formating are concatenated. Note: The accuracy of the content display may be affected if this property is set to ``True``. |
| [page_horizontal_alignment](./page_horizontal_alignment/) | Specifies the horizontal alignment of pages in an HTML document. Default value is [HtmlFixedPageHorizontalAlignment.CENTER](../htmlfixedpagehorizontalalignment/#CENTER). |
| [page_margins](./page_margins/) | Specifies the margins around pages in an HTML document. The margins value is measured in points and should be equal to or greater than 0. Default value is 10 points. |
| [page_saving_callback](../fixedpagesaveoptions/page_saving_callback/) | Allows to control how separate pages are saved when a document is exported to fixed page format.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [page_set](../fixedpagesaveoptions/page_set/) | Gets or sets the pages to render. Default is all the pages in the document.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [pretty_format](../saveoptions/pretty_format/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progress_callback](../saveoptions/progress_callback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [resource_saving_callback](./resource_saving_callback/) | Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format. |
| [resources_folder](./resources_folder/) | Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. Default is ``None``. |
| [resources_folder_alias](./resources_folder_alias/) | Specifies the name of the folder used to construct image URIs written into an Html document. Default is ``None``. |
| [save_font_face_css_separately](./save_font_face_css_separately/) | Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css" when a document is being saved with external stylesheet (that is, when [HtmlFixedSaveOptions.export_embedded_css](./export_embedded_css/) is ``False``). Default value is ``False``, all CSS rules are written into single file "styles.css". |
| [save_format](./save_format/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.HTML_FIXED](../../aspose.words/saveformat/#HTML_FIXED). |
| [show_page_border](./show_page_border/) | Specifies whether border around pages should be shown. Default is ``True``. |
| [temp_folder](../saveoptions/temp_folder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``None`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_created_time_property](../saveoptions/update_created_time_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.created_time](../../aspose.words.properties/builtindocumentproperties/created_time/) property is updated before saving. Default value is ``False``;<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_fields](../saveoptions/update_fields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_last_printed_property](../saveoptions/update_last_printed_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.last_printed](../../aspose.words.properties/builtindocumentproperties/last_printed/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_last_saved_time_property](../saveoptions/update_last_saved_time_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.last_saved_time](../../aspose.words.properties/builtindocumentproperties/last_saved_time/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_sdt_content](../saveoptions/update_sdt_content/) | Gets or sets value determining whether content of [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [use_anti_aliasing](../saveoptions/use_anti_aliasing/) | Gets or sets a value determining whether or not to use anti-aliasing for rendering.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [use_high_quality_rendering](../saveoptions/use_high_quality_rendering/) | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [use_target_machine_fonts](./use_target_machine_fonts/) | Flag indicates whether fonts from target machine must be used to display the document. If this flag is set to ``True``, [HtmlFixedSaveOptions.font_format](./font_format/) and [HtmlFixedSaveOptions.export_embedded_fonts](./export_embedded_fonts/) properties do not have effect, also [HtmlFixedSaveOptions.resource_saving_callback](./resource_saving_callback/) is not fired for fonts. Default is ``False``. |

### Methods

| Name | Description |
| --- | --- |
|[ create_save_options(save_format)](../saveoptions/create_save_options/#saveformat) | Creates a save options object of a class suitable for the specified save format.<br>(Inherited from [SaveOptions](../saveoptions/)) |
|[ create_save_options(file_name)](../saveoptions/create_save_options/#str) | Creates a save options object of a class suitable for the file extension specified in the given file name.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### See Also

* module [aspose.words.saving](../)
* class [FixedPageSaveOptions](../fixedpagesaveoptions/)

