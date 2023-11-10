---
title: OdtSaveOptions class
linktitle: OdtSaveOptions class
articleTitle: OdtSaveOptions class
second_title: Aspose.Words for Python
description: "aspose.words.saving.OdtSaveOptions class. Can be used to specify additional options when saving a document into the [SaveFormat.ODT](../../aspose.words/saveformat/#ODT) or [SaveFormat.OTT](../../aspose.words/saveformat/#OTT) format"
type: docs
weight: 480
url: /python-net/aspose.words.saving/odtsaveoptions/
---

## OdtSaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.ODT](../../aspose.words/saveformat/#ODT) or
[SaveFormat.OTT](../../aspose.words/saveformat/#OTT) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/python-net/specify-save-options/) documentation article.




### Remarks

At the moment provides only the [OdtSaveOptions.save_format](./save_format/) property, but in the future will have 
other options added, such as an encryption password or digital signature settings.




**Inheritance:** [OdtSaveOptions](./) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [OdtSaveOptions()](./__init__/#default) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.ODT](../../aspose.words/saveformat/#ODT) format. |
| [OdtSaveOptions(password)](./__init__/#str) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.ODT](../../aspose.words/saveformat/#ODT) format encrypted with a password. |
| [OdtSaveOptions(save_format)](./__init__/#saveformat) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.ODT](../../aspose.words/saveformat/#ODT) or [SaveFormat.OTT](../../aspose.words/saveformat/#OTT) format. |

### Properties

| Name | Description |
| --- | --- |
| [allow_embedding_post_script_fonts](../saveoptions/allow_embedding_post_script_fonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [default_template](../saveoptions/default_template/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_3d_effects_rendering_mode](../saveoptions/dml_3d_effects_rendering_mode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_effects_rendering_mode](../saveoptions/dml_effects_rendering_mode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_rendering_mode](../saveoptions/dml_rendering_mode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [export_generator_name](../saveoptions/export_generator_name/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [iml_rendering_mode](../saveoptions/iml_rendering_mode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [is_strict_schema11](./is_strict_schema11/) | Specifies whether export should correspond to ODT specification 1.1 strictly.  OOo 3.0 displays files correctly when they contain elements and attributes of ODT 1.2.  Use "false" for this purpose, or "true" for strict conformity of specification 1.1. The default value is ``False``. |
| [measure_unit](./measure_unit/) | Allows to specify units of measure to apply to document content. The default value is [OdtSaveMeasureUnit.CENTIMETERS](../odtsavemeasureunit/#CENTIMETERS) |
| [memory_optimization](../saveoptions/memory_optimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [password](./password/) | Gets or sets a password to encrypt document. |
| [pretty_format](../saveoptions/pretty_format/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progress_callback](../saveoptions/progress_callback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [save_format](./save_format/) | Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.ODT](../../aspose.words/saveformat/#ODT) or [SaveFormat.OTT](../../aspose.words/saveformat/#OTT). |
| [temp_folder](../saveoptions/temp_folder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``None`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
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

### Examples

Shows how to make a saved document conform to an older ODT schema.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

save_options = aw.saving.OdtSaveOptions()
save_options.measure_unit = aw.saving.OdtSaveMeasureUnit.CENTIMETERS
save_options.is_strict_schema11 = export_to_odt11_specs

doc.save(ARTIFACTS_DIR + "OdtSaveOptions.odt11_schema.odt", save_options)
```

Shows how to use different measurement units to define style parameters of a saved ODT document.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

# When we export the document to .odt, we can use an OdtSaveOptions object to modify how we save the document.
# We can set the "measure_unit" property to "OdtSaveMeasureUnit.CENTIMETERS"
# to define content such as style parameters using the metric system, which Open Office uses.
# We can set the "measure_unit" property to "OdtSaveMeasureUnit.INCHES"
# to define content such as style parameters using the imperial system, which Microsoft Word uses.
save_options = aw.saving.OdtSaveOptions()
save_options.measure_unit = odt_save_measure_unit

doc.save(ARTIFACTS_DIR + "OdtSaveOptions.measurement_units.odt", save_options)
```

### See Also

* module [aspose.words.saving](../)
* class [SaveOptions](../saveoptions/)

