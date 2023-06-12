﻿---
title: PclSaveOptions class
linktitle: PclSaveOptions class
articleTitle: PclSaveOptions class
second_title: Aspose.Words for Python
description: "aspose.words.saving.PclSaveOptions class. Can be used to specify additional options when saving a document into the [SaveFormat.PCL](../../aspose.words/saveformat/#PCL) format"
type: docs
weight: 550
url: /python-net/aspose.words.saving/pclsaveoptions/
---

## PclSaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.PCL](../../aspose.words/saveformat/#PCL) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/python-net/specify-save-options/) documentation article.




**Inheritance:** [PclSaveOptions](./) → [FixedPageSaveOptions](../fixedpagesaveoptions/) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [PclSaveOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [allow_embedding_post_script_fonts](../saveoptions/allow_embedding_post_script_fonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [color_mode](../fixedpagesaveoptions/color_mode/) | Gets or sets a value determining how colors are rendered.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [default_template](../saveoptions/default_template/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** (System.String.Empty).<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_3d_effects_rendering_mode](../saveoptions/dml_3d_effects_rendering_mode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_effects_rendering_mode](../saveoptions/dml_effects_rendering_mode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_rendering_mode](../saveoptions/dml_rendering_mode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [export_generator_name](../saveoptions/export_generator_name/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [fallback_font_name](./fallback_font_name/) | Name of the font that will be used if no expected font is found in printer and built-in fonts collections. |
| [iml_rendering_mode](../saveoptions/iml_rendering_mode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [jpeg_quality](../fixedpagesaveoptions/jpeg_quality/) | Gets or sets a value determining the quality of the JPEG images inside Html document.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [memory_optimization](../saveoptions/memory_optimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [metafile_rendering_options](../fixedpagesaveoptions/metafile_rendering_options/) | Allows to specify metafile rendering options.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [numeral_format](../fixedpagesaveoptions/numeral_format/) | Gets or sets [NumeralFormat](../numeralformat/) used for rendering of numerals. European numerals are used by default.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [optimize_output](../fixedpagesaveoptions/optimize_output/) | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to ``True``.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [page_saving_callback](../fixedpagesaveoptions/page_saving_callback/) | Allows to control how separate pages are saved when a document is exported to fixed page format.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [page_set](../fixedpagesaveoptions/page_set/) | Gets or sets the pages to render. Default is all the pages in the document.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [pretty_format](../saveoptions/pretty_format/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progress_callback](../saveoptions/progress_callback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [rasterize_transformed_elements](./rasterize_transformed_elements/) | Gets or sets a value determining whether or not complex transformed elements should be rasterized before saving to PCL document. Default is ``True``. |
| [save_format](./save_format/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.PCL](../../aspose.words/saveformat/#PCL). |
| [temp_folder](../saveoptions/temp_folder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``None`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_created_time_property](../saveoptions/update_created_time_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.created_time](../../aspose.words.properties/builtindocumentproperties/created_time/) property is updated before saving. Default value is ``False``;<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_fields](../saveoptions/update_fields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_last_printed_property](../saveoptions/update_last_printed_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.last_printed](../../aspose.words.properties/builtindocumentproperties/last_printed/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_last_saved_time_property](../saveoptions/update_last_saved_time_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.last_saved_time](../../aspose.words.properties/builtindocumentproperties/last_saved_time/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_sdt_content](../saveoptions/update_sdt_content/) | Gets or sets value determining whether content of [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [use_anti_aliasing](../saveoptions/use_anti_aliasing/) | Gets or sets a value determining whether or not to use anti-aliasing for rendering.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [use_high_quality_rendering](../saveoptions/use_high_quality_rendering/) | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Methods

| Name | Description |
| --- | --- |
|[ add_printer_font(font_full_name, font_pcl_name)](./add_printer_font/#str_str) | Adds information about font that is uploaded to the printer by manufacturer. |
|[ create_save_options(save_format)](../saveoptions/create_save_options/#saveformat) | Creates a save options object of a class suitable for the specified save format.<br>(Inherited from [SaveOptions](../saveoptions/)) |
|[ create_save_options(file_name)](../saveoptions/create_save_options/#str) | Creates a save options object of a class suitable for the file extension specified in the given file name.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Examples

Shows how to rasterize complex elements while saving a document to PCL.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

save_options = aw.saving.PclSaveOptions()
save_options.save_format = aw.SaveFormat.PCL
save_options.rasterize_transformed_elements = True

doc.save(ARTIFACTS_DIR + "PclSaveOptions.rasterize_elements.pcl", save_options)
```

### See Also

* module [aspose.words.saving](../)
* class [FixedPageSaveOptions](../fixedpagesaveoptions/)

