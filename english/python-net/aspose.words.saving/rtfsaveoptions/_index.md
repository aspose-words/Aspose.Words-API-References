---
title: RtfSaveOptions class
second_title: Aspose.Words for Python via .NET API Reference
description: "Can be used to specify additional options when saving a document into the [SaveFormat.RTF](../../aspose.words/saveformat/#RTF) format."
type: docs
weight: 700
url: /python-net/aspose.words.saving/rtfsaveoptions/
---

## RtfSaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.RTF](../../aspose.words/saveformat/#RTF) format.



**Inheritance:** [RtfSaveOptions](./) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [RtfSaveOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [allow_embedding_post_script_fonts](../saveoptions/allow_embedding_post_script_fonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [default_template](../saveoptions/default_template/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** (System.String.Empty).<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_3d_effects_rendering_mode](../saveoptions/dml_3d_effects_rendering_mode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_effects_rendering_mode](../saveoptions/dml_effects_rendering_mode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_rendering_mode](../saveoptions/dml_rendering_mode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [export_compact_size](./export_compact_size/) | Allows to make output RTF documents smaller in size, but if they contain  RTL (right-to-left) text, it will not be displayed correctly. |
| [export_generator_name](../saveoptions/export_generator_name/) | When true, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [export_images_for_old_readers](./export_images_for_old_readers/) | Specifies whether the keywords for "old readers" are written to RTF or not. This can significantly affect the size of the RTF document. |
| [flat_opc_xml_mapping_only](../saveoptions/flat_opc_xml_mapping_only/) | Gets or sets value determining which document formats are allowed to be mapped by [StructuredDocumentTag.xml_mapping](../../aspose.words.markup/structureddocumenttag/xml_mapping/). By default only [LoadFormat.FLAT_OPC](../../aspose.words/loadformat/#FLAT_OPC) document format is allowed to be mapped.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [iml_rendering_mode](../saveoptions/iml_rendering_mode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [memory_optimization](../saveoptions/memory_optimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [pretty_format](../saveoptions/pretty_format/) | When ``true``, pretty formats output where applicable.  Default value is **false**.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progress_callback](../saveoptions/progress_callback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [save_format](./save_format/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.RTF](../../aspose.words/saveformat/#RTF). |
| [save_images_as_wmf](./save_images_as_wmf/) | When true all images will be saved as WMF. |
| [temp_folder](../saveoptions/temp_folder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``null`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_created_time_property](../saveoptions/update_created_time_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.created_time](../../aspose.words.properties/builtindocumentproperties/created_time/) property is updated before saving. Default value is false;<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_fields](../saveoptions/update_fields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_last_printed_property](../saveoptions/update_last_printed_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.last_printed](../../aspose.words.properties/builtindocumentproperties/last_printed/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_last_saved_time_property](../saveoptions/update_last_saved_time_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.last_saved_time](../../aspose.words.properties/builtindocumentproperties/last_saved_time/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_sdt_content](../saveoptions/update_sdt_content/) | Gets or sets value determining whether content of [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [use_anti_aliasing](../saveoptions/use_anti_aliasing/) | Gets or sets a value determining whether or not to use anti-aliasing for rendering.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [use_high_quality_rendering](../saveoptions/use_high_quality_rendering/) | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Methods

| Name | Description |
| --- | --- |
|[ create_save_options(save_format)](../saveoptions/create_save_options/#saveformat) | Creates a save options object of a class suitable for the specified save format.<br>(Inherited from [SaveOptions](../saveoptions/)) |
|[ create_save_options(file_name)](../saveoptions/create_save_options/#str) | Creates a save options object of a class suitable for the file extension specified in the given file name.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Examples

Shows how to save a document to .rtf with custom options.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

# Create an "RtfSaveOptions" object to pass to the document's "save" method to modify how we save it to an RTF.
options = aw.saving.RtfSaveOptions()

self.assertEqual(aw.SaveFormat.RTF, options.save_format)

# Set the "export_compact_size" property to "True" to
# reduce the saved document's size at the cost of right-to-left text compatibility.
options.export_compact_size = True

# Set the "export_images_for_old_readers" property to "True" to use extra keywords to ensure that our document is
# compatible with pre-Microsoft Word 97 readers and WordPad.
# Set the "export_images_for_old_readers" property to "False" to reduce the size of the document,
# but prevent old readers from being able to read any non-metafile or BMP images that the document may contain.
options.export_images_for_old_readers = export_images_for_old_readers

doc.save(ARTIFACTS_DIR + "RtfSaveOptions.export_images.rtf", options)
```

### See Also

* module [aspose.words.saving](../)
* class [SaveOptions](../saveoptions/)

