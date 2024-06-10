---
title: DocSaveOptions class
linktitle: DocSaveOptions class
articleTitle: DocSaveOptions class
second_title: Aspose.Words for Python
description: "aspose.words.saving.DocSaveOptions class. Can be used to specify additional options when saving a document into the [SaveFormat.DOC](../../aspose.words/saveformat/#DOC) or [SaveFormat.DOT](../../aspose.words/saveformat/#DOT) format"
type: docs
weight: 100
url: /python-net/aspose.words.saving/docsaveoptions/
---

## DocSaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.DOC](../../aspose.words/saveformat/#DOC) or
[SaveFormat.DOT](../../aspose.words/saveformat/#DOT) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/python-net/specify-save-options/) documentation article.




### Remarks

At the moment provides only the [DocSaveOptions.save_format](./save_format/) property, but in the future will have
other options added, such as an encryption password or digital signature settings.




**Inheritance:** [DocSaveOptions](./) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [DocSaveOptions()](./__init__/#default) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.DOC](../../aspose.words/saveformat/#DOC) format. |
| [DocSaveOptions(save_format)](./__init__/#saveformat) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.DOC](../../aspose.words/saveformat/#DOC) or [SaveFormat.DOT](../../aspose.words/saveformat/#DOT) format. |

### Properties

| Name | Description |
| --- | --- |
| [allow_embedding_post_script_fonts](../saveoptions/allow_embedding_post_script_fonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [always_compress_metafiles](./always_compress_metafiles/) | When ``False``, small metafiles are not compressed for performance reason. Default value is ``True``, all metafiles are compressed regardless of its size. |
| [default_template](../saveoptions/default_template/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [digital_signature_details](./digital_signature_details/) | Gets or sets [DigitalSignatureDetails](../digitalsignaturedetails/) object used to sign a document. |
| [dml_3d_effects_rendering_mode](../saveoptions/dml_3d_effects_rendering_mode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_effects_rendering_mode](../saveoptions/dml_effects_rendering_mode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_rendering_mode](../saveoptions/dml_rendering_mode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [export_generator_name](../saveoptions/export_generator_name/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [iml_rendering_mode](../saveoptions/iml_rendering_mode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [memory_optimization](../saveoptions/memory_optimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [password](./password/) | Gets/sets a password to encrypt document using RC4 encryption method. |
| [pretty_format](../saveoptions/pretty_format/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progress_callback](../saveoptions/progress_callback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [save_format](./save_format/) | Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.DOC](../../aspose.words/saveformat/#DOC) or [SaveFormat.DOT](../../aspose.words/saveformat/#DOT). |
| [save_picture_bullet](./save_picture_bullet/) | When ``False``, PictureBullet data is not saved to output document. Default value is ``True``. |
| [save_routing_slip](./save_routing_slip/) | When ``False``, RoutingSlip data is not saved to output document. Default value is ``True``. |
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

Shows how to set save options for older Microsoft Word formats.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('Hello world!')
options = aw.saving.DocSaveOptions(aw.SaveFormat.DOC)
# Set a password which will protect the loading of the document by Microsoft Word or Aspose.Words.
# Note that this does not encrypt the contents of the document in any way.
options.password = 'MyPassword'
# If the document contains a routing slip, we can preserve it while saving by setting this flag to True.
options.save_routing_slip = True
doc.save(ARTIFACTS_DIR + 'DocSaveOptions.save_as_doc.doc', options)
# To be able to load the document,
# we will need to apply the password we specified in the DocSaveOptions object in a LoadOptions object.
with self.assertRaises(Exception):
    doc = aw.Document(ARTIFACTS_DIR + 'DocSaveOptions.save_as_doc.doc')
load_options = aw.loading.LoadOptions('MyPassword')
doc = aw.Document(ARTIFACTS_DIR + 'DocSaveOptions.save_as_doc.doc', load_options)
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words.saving](../)
* class [SaveOptions](../saveoptions/)

