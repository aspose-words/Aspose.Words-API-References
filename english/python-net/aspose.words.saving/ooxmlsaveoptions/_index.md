---
title: OoxmlSaveOptions class
second_title: Aspose.Words for Python via .NET API Reference
description: "Can be used to specify additional options when saving a document into the [SaveFormat.DOCX](../../aspose.words/saveformat/#DOCX), [SaveFormat.DOCM](../../aspose.words/saveformat/#DOCM), [SaveFormat.DOTX](../../aspose.words/saveformat/#DOTX), [SaveFormat.DOTM](../../aspose.words/saveformat/#DOTM) or [SaveFormat.FLAT_OPC](../../aspose.words/saveformat/#FLAT_OPC) format"
type: docs
weight: 490
url: /python-net/aspose.words.saving/ooxmlsaveoptions/
---

## OoxmlSaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.DOCX](../../aspose.words/saveformat/#DOCX),
[SaveFormat.DOCM](../../aspose.words/saveformat/#DOCM), [SaveFormat.DOTX](../../aspose.words/saveformat/#DOTX), [SaveFormat.DOTM](../../aspose.words/saveformat/#DOTM) or
[SaveFormat.FLAT_OPC](../../aspose.words/saveformat/#FLAT_OPC) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/net/specify-save-options/) documentation article.




**Inheritance:** [OoxmlSaveOptions](./) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [OoxmlSaveOptions()](./__init__/#default) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.DOCX](../../aspose.words/saveformat/#DOCX) format. |
| [OoxmlSaveOptions(save_format)](./__init__/#saveformat) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.DOCX](../../aspose.words/saveformat/#DOCX), [SaveFormat.DOCM](../../aspose.words/saveformat/#DOCM), [SaveFormat.DOTX](../../aspose.words/saveformat/#DOTX), [SaveFormat.DOTM](../../aspose.words/saveformat/#DOTM) or [SaveFormat.FLAT_OPC](../../aspose.words/saveformat/#FLAT_OPC) format. |

### Properties

| Name | Description |
| --- | --- |
| [allow_embedding_post_script_fonts](../saveoptions/allow_embedding_post_script_fonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [compliance](./compliance/) | Specifies the OOXML version for the output document. The default value is [OoxmlCompliance.ECMA376_2006](../ooxmlcompliance/#ECMA376_2006). |
| [compression_level](./compression_level/) | Specifies the compression level used to save document. The default value is [CompressionLevel.NORMAL](../compressionlevel/#NORMAL). |
| [default_template](../saveoptions/default_template/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** (System.String.Empty).<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_3d_effects_rendering_mode](../saveoptions/dml_3d_effects_rendering_mode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_effects_rendering_mode](../saveoptions/dml_effects_rendering_mode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_rendering_mode](../saveoptions/dml_rendering_mode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [export_generator_name](../saveoptions/export_generator_name/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [iml_rendering_mode](../saveoptions/iml_rendering_mode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [keep_legacy_control_chars](./keep_legacy_control_chars/) | Keeps original representation of legacy control characters. |
| [memory_optimization](../saveoptions/memory_optimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [password](./password/) | Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm. |
| [pretty_format](../saveoptions/pretty_format/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progress_callback](../saveoptions/progress_callback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [save_format](./save_format/) | Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.DOCX](../../aspose.words/saveformat/#DOCX), [SaveFormat.DOCM](../../aspose.words/saveformat/#DOCM), [SaveFormat.DOTX](../../aspose.words/saveformat/#DOTX), [SaveFormat.DOTM](../../aspose.words/saveformat/#DOTM) or [SaveFormat.FLAT_OPC](../../aspose.words/saveformat/#FLAT_OPC). |
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
|[ create_save_options(save_format)](../saveoptions/create_save_options/#saveformat) | Creates a save options object of a class suitable for the specified save format.<br>(Inherited from [SaveOptions](../saveoptions/)) |
|[ create_save_options(file_name)](../saveoptions/create_save_options/#str) | Creates a save options object of a class suitable for the file extension specified in the given file name.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Examples

Shows how to set an OOXML compliance specification for a saved document to adhere to.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# If we configure compatibility options to comply with Microsoft Word 2003,
# inserting an image will define its shape using VML.
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2003)
builder.insert_image(IMAGE_DIR + "Transparent background logo.png")

self.assertEqual(aw.drawing.ShapeMarkupLanguage.VML, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().markup_language)

# The "ISO/IEC 29500:2008" OOXML standard does not support VML shapes.
# If we set the "compliance" property of the SaveOptions object to "OoxmlCompliance.ISO29500_2008_STRICT",
# any document we save while passing this object will have to follow that standard.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
save_options.save_format = aw.SaveFormat.DOCX

doc.save(ARTIFACTS_DIR + "OoxmlSaveOptions.iso29500_strict.docx", save_options)

# Our saved document defines the shape using DML to adhere to the "ISO/IEC 29500:2008" OOXML standard.
doc = aw.Document(ARTIFACTS_DIR + "OoxmlSaveOptions.iso29500_strict.docx")

self.assertEqual(aw.drawing.ShapeMarkupLanguage.DML, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().markup_language)
```

### See Also

* module [aspose.words.saving](../)
* class [SaveOptions](../saveoptions/)

