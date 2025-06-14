﻿---
title: WordML2003SaveOptions class
linktitle: WordML2003SaveOptions class
articleTitle: WordML2003SaveOptions class
second_title: Aspose.Words for Python
description: "aspose.words.saving.WordML2003SaveOptions class. Can be used to specify additional options when saving a document into the [SaveFormat.WORD_ML](../../aspose.words/saveformat/#WORD_ML) format"
type: docs
weight: 900
url: /python-net/aspose.words.saving/wordml2003saveoptions/
---

## WordML2003SaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.WORD_ML](../../aspose.words/saveformat/#WORD_ML) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/python-net/specify-save-options/) documentation article.




### Remarks

At the moment provides only the [WordML2003SaveOptions.save_format](./save_format/) property, but in the future may have other options added.




**Inheritance:** [WordML2003SaveOptions](./) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [WordML2003SaveOptions()](./__init__/#default) | The default constructor. |

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
| [memory_optimization](../saveoptions/memory_optimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [pretty_format](../saveoptions/pretty_format/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progress_callback](../saveoptions/progress_callback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [save_format](./save_format/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.WORD_ML](../../aspose.words/saveformat/#WORD_ML). |
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

### Examples

Shows how to manage output document's raw content.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Create a "WordML2003SaveOptions" object to pass to the document's "Save" method
# to modify how we save the document to the WordML save format.
options = aw.saving.WordML2003SaveOptions()
self.assertEqual(aw.SaveFormat.WORD_ML, options.save_format)
# Set the "PrettyFormat" property to "true" to apply tab character indentation and
# newlines to make the output document's raw content easier to read.
# Set the "PrettyFormat" property to "false" to save the document's raw content in one continuous body of the text.
options.pretty_format = pretty_format
doc.save(file_name=ARTIFACTS_DIR + 'WordML2003SaveOptions.PrettyFormat.xml', save_options=options)
file_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'WordML2003SaveOptions.PrettyFormat.xml')
new_line = system_helper.environment.Environment.new_line()
if pretty_format:
    self.assertTrue(f'<o:DocumentProperties>{new_line}\t\t' + f'<o:Revision>1</o:Revision>{new_line}\t\t' + f'<o:TotalTime>0</o:TotalTime>{new_line}\t\t' + f'<o:Pages>1</o:Pages>{new_line}\t\t' + f'<o:Words>0</o:Words>{new_line}\t\t' + f'<o:Characters>0</o:Characters>{new_line}\t\t' + f'<o:Lines>1</o:Lines>{new_line}\t\t' + f'<o:Paragraphs>1</o:Paragraphs>{new_line}\t\t' + f'<o:CharactersWithSpaces>0</o:CharactersWithSpaces>{new_line}\t\t' + f'<o:Version>11.5606</o:Version>{new_line}\t' + '</o:DocumentProperties>' in file_contents)
else:
    self.assertTrue('<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>' + '<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>' + '<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>' in file_contents)
```

Shows how to manage memory optimization.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Create a "WordML2003SaveOptions" object to pass to the document's "Save" method
# to modify how we save the document to the WordML save format.
options = aw.saving.WordML2003SaveOptions()
# Set the "MemoryOptimization" flag to "true" to decrease memory consumption
# during the document's saving operation at the cost of a longer saving time.
# Set the "MemoryOptimization" flag to "false" to save the document normally.
options.memory_optimization = memory_optimization
doc.save(file_name=ARTIFACTS_DIR + 'WordML2003SaveOptions.MemoryOptimization.xml', save_options=options)
```

### See Also

* module [aspose.words.saving](../)
* class [SaveOptions](../saveoptions/)

