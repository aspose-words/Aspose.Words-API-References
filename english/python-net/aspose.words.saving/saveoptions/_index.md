---
title: SaveOptions class
second_title: Aspose.Words for Python via .NET API Reference
description: "This is an abstract base class for classes that allow the user to specify additional options when saving a document into a particular format"
type: docs
weight: 720
url: /python-net/aspose.words.saving/saveoptions/
---

## SaveOptions class

This is an abstract base class for classes that allow the user to specify additional
options when saving a document into a particular format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/python-net/specify-save-options/) documentation article.




An instance of the [SaveOptions](./) class or any derived class is passed to the stream [Document.save()](../../aspose.words/document/save/#bytesio_saveoptions)
or string [Document.save()](../../aspose.words/document/save/#str_saveoptions) overloads for the user to define custom options when saving a document.



### Properties

| Name | Description |
| --- | --- |
| [allow_embedding_post_script_fonts](./allow_embedding_post_script_fonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``. |
| [default_template](./default_template/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** (System.String.Empty). |
| [dml_3d_effects_rendering_mode](./dml_3d_effects_rendering_mode/) | Gets or sets a value determining how 3D effects are rendered. |
| [dml_effects_rendering_mode](./dml_effects_rendering_mode/) | Gets or sets a value determining how DrawingML effects are rendered. |
| [dml_rendering_mode](./dml_rendering_mode/) | Gets or sets a value determining how DrawingML shapes are rendered. |
| [export_generator_name](./export_generator_name/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``. |
| [iml_rendering_mode](./iml_rendering_mode/) | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [memory_optimization](./memory_optimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``. |
| [pretty_format](./pretty_format/) | When ``True``, pretty formats output where applicable. Default value is ``False``. |
| [progress_callback](./progress_callback/) | Called during saving a document and accepts data about saving progress. |
| [save_format](./save_format/) | Specifies the format in which the document will be saved if this save options object is used. |
| [temp_folder](./temp_folder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``None`` and no temporary files are used. |
| [update_created_time_property](./update_created_time_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.created_time](../../aspose.words.properties/builtindocumentproperties/created_time/) property is updated before saving. Default value is ``False``; |
| [update_fields](./update_fields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is ``True``. |
| [update_last_printed_property](./update_last_printed_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.last_printed](../../aspose.words.properties/builtindocumentproperties/last_printed/) property is updated before saving. |
| [update_last_saved_time_property](./update_last_saved_time_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.last_saved_time](../../aspose.words.properties/builtindocumentproperties/last_saved_time/) property is updated before saving. |
| [update_sdt_content](./update_sdt_content/) | Gets or sets value determining whether content of [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) is updated before saving. |
| [use_anti_aliasing](./use_anti_aliasing/) | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [use_high_quality_rendering](./use_high_quality_rendering/) | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |

### Methods

| Name | Description |
| --- | --- |
|[ create_save_options(save_format)](./create_save_options/#saveformat) | Creates a save options object of a class suitable for the specified save format. |
|[ create_save_options(file_name)](./create_save_options/#str) | Creates a save options object of a class suitable for the file extension specified in the given file name. |

### Examples

Shows how to use a specific encoding when saving a document to .epub.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

# Use a SaveOptions object to specify the encoding for a document that we will save.
save_options = aw.saving.HtmlSaveOptions()
save_options.save_format = aw.SaveFormat.EPUB
save_options.encoding = "utf-8"

# By default, an output .epub document will have all its contents in one HTML part.
# A split criterion allows us to segment the document into several HTML parts.
# We will set the criteria to split the document into heading paragraphs.
# This is useful for readers who cannot read HTML files more significant than a specific size.
save_options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH

# Specify that we want to export document properties.
save_options.export_document_properties = True

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.doc2_epub_save_options.epub", save_options)
```

### See Also

* module [aspose.words.saving](../)

