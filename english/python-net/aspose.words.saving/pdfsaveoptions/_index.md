---
title: PdfSaveOptions class
linktitle: PdfSaveOptions class
articleTitle: PdfSaveOptions class
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfSaveOptions class. Can be used to specify additional options when saving a document into the [SaveFormat.PDF](../../aspose.words/saveformat/#PDF) format"
type: docs
weight: 740
url: /python-net/aspose.words.saving/pdfsaveoptions/
---

## PdfSaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.PDF](../../aspose.words/saveformat/#PDF) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/python-net/specify-save-options/) documentation article.




**Inheritance:** [PdfSaveOptions](./) → [FixedPageSaveOptions](../fixedpagesaveoptions/) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [PdfSaveOptions()](./__init__/#default) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.PDF](../../aspose.words/saveformat/#PDF) format. |

### Properties

| Name | Description |
| --- | --- |
| [additional_text_positioning](./additional_text_positioning/) | A flag specifying whether to write additional text positioning operators or not. |
| [allow_embedding_post_script_fonts](../saveoptions/allow_embedding_post_script_fonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [attachments_embedding_mode](./attachments_embedding_mode/) | Gets or sets a value determining how attachments are embedded to the PDF document. |
| [cache_background_graphics](./cache_background_graphics/) | Gets or sets a value determining whether or not to cache graphics placed in document's background. |
| [color_mode](../fixedpagesaveoptions/color_mode/) | Gets or sets a value determining how colors are rendered.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [compliance](./compliance/) | Specifies the PDF standards compliance level for output documents. |
| [create_note_hyperlinks](./create_note_hyperlinks/) | Specifies whether to convert footnote/endnote references in main text story into active hyperlinks. When clicked the hyperlink will lead to the corresponding footnote/endnote. Default is ``False``. |
| [custom_properties_export](./custom_properties_export/) | Gets or sets a value determining the way [Document.custom_document_properties](../../aspose.words/document/custom_document_properties/) are exported to PDF file. |
| [default_template](../saveoptions/default_template/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [digital_signature_details](./digital_signature_details/) | Gets or sets the details for signing the output PDF document. |
| [display_doc_title](./display_doc_title/) | A flag specifying whether the window’s title bar should display the document title taken from the Title entry of the document information dictionary. |
| [dml_3d_effects_rendering_mode](../saveoptions/dml_3d_effects_rendering_mode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_effects_rendering_mode](./dml_effects_rendering_mode/) | Gets or sets a value determining how DrawingML effects are rendered. |
| [dml_rendering_mode](../saveoptions/dml_rendering_mode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [downsample_options](./downsample_options/) | Allows to specify downsample options. |
| [embed_full_fonts](./embed_full_fonts/) | Controls how fonts are embedded into the resulting PDF documents. |
| [encryption_details](./encryption_details/) | Gets or sets the details for encrypting the output PDF document. |
| [export_document_structure](./export_document_structure/) | Gets or sets a value determining whether or not to export document structure. |
| [export_floating_shapes_as_inline_tag](./export_floating_shapes_as_inline_tag/) | Gets or sets a value determining whether floating shapes are exported as inline tags in the document structure. |
| [export_generator_name](../saveoptions/export_generator_name/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [export_language_to_span_tag](./export_language_to_span_tag/) | Gets or sets a value determining whether or not to create a "Span" tag in the document structure to export the text language. |
| [export_paragraph_graphics_to_artifact](./export_paragraph_graphics_to_artifact/) | Gets or sets a value determining whether a paragraph graphic should be marked as an artifact. |
| [font_embedding_mode](./font_embedding_mode/) | Specifies the font embedding mode. |
| [header_footer_bookmarks_export_mode](./header_footer_bookmarks_export_mode/) | Determines how bookmarks in headers/footers are exported. |
| [image_color_space_export_mode](./image_color_space_export_mode/) | Specifies how the color space will be selected for the images in PDF document. |
| [image_compression](./image_compression/) | Specifies compression type to be used for all images in the document. |
| [iml_rendering_mode](../saveoptions/iml_rendering_mode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [interpolate_images](./interpolate_images/) | A flag indicating whether image interpolation shall be performed by a conforming reader. When ``False`` is specified, the flag is not written to the output document and the default behaviour of reader is used instead. |
| [jpeg_quality](./jpeg_quality/) | Gets or sets a value determining the quality of the JPEG images inside PDF document. |
| [memory_optimization](../saveoptions/memory_optimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [metafile_rendering_options](../fixedpagesaveoptions/metafile_rendering_options/) | Allows to specify metafile rendering options.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [numeral_format](../fixedpagesaveoptions/numeral_format/) | Gets or sets [NumeralFormat](../numeralformat/) used for rendering of numerals. European numerals are used by default.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [open_hyperlinks_in_new_window](./open_hyperlinks_in_new_window/) | Gets or sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser. |
| [optimize_output](../fixedpagesaveoptions/optimize_output/) | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to ``True``.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [outline_options](./outline_options/) | Allows to specify outline options. |
| [page_layout](./page_layout/) | Specifies the page layout to be used when the document is opened in a PDF reader. |
| [page_mode](./page_mode/) | Specifies how the PDF document should be displayed when opened in a PDF reader. |
| [page_saving_callback](../fixedpagesaveoptions/page_saving_callback/) | Allows to control how separate pages are saved when a document is exported to fixed page format.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [page_set](../fixedpagesaveoptions/page_set/) | Gets or sets the pages to render. Default is all the pages in the document.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [preblend_images](./preblend_images/) | Gets or sets a value determining whether or not to preblend transparent images with black background color. |
| [preserve_form_fields](./preserve_form_fields/) | Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text. Default is ``False``. |
| [pretty_format](../saveoptions/pretty_format/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progress_callback](../saveoptions/progress_callback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [render_choice_form_field_border](./render_choice_form_field_border/) | Specifies whether to render PDF choice form field border. |
| [save_format](./save_format/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.PDF](../../aspose.words/saveformat/#PDF). |
| [temp_folder](../saveoptions/temp_folder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``None`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [text_compression](./text_compression/) | Specifies compression type to be used for all textual content in the document. |
| [update_ambiguous_text_font](../saveoptions/update_ambiguous_text_font/) | Determines whether the font attributes will be changed according to the character code being used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_created_time_property](../saveoptions/update_created_time_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.created_time](../../aspose.words.properties/builtindocumentproperties/created_time/) property is updated before saving. Default value is ``False``;<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_fields](../saveoptions/update_fields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_last_printed_property](../saveoptions/update_last_printed_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.last_printed](../../aspose.words.properties/builtindocumentproperties/last_printed/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_last_saved_time_property](../saveoptions/update_last_saved_time_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.last_saved_time](../../aspose.words.properties/builtindocumentproperties/last_saved_time/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [use_anti_aliasing](../saveoptions/use_anti_aliasing/) | Gets or sets a value determining whether or not to use anti-aliasing for rendering.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [use_book_fold_printing_settings](./use_book_fold_printing_settings/) | Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.multiple_pages](../../aspose.words/pagesetup/multiple_pages/). |
| [use_core_fonts](./use_core_fonts/) | Gets or sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts. |
| [use_high_quality_rendering](../saveoptions/use_high_quality_rendering/) | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [use_sdt_tag_as_form_field_name](./use_sdt_tag_as_form_field_name/) | Specifies whether to use SDT control Tag or Id property as a name of form field in PDF. |
| [zoom_behavior](./zoom_behavior/) | Gets or sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer. |
| [zoom_factor](./zoom_factor/) | Gets or sets a value determining zoom factor (in percentages) for a document. |

### Methods

| Name | Description |
| --- | --- |
|[ clone()](./clone/#default) | Creates a deep clone of this object. |
|[ create_save_options(save_format)](../saveoptions/create_save_options/#saveformat) | Creates a save options object of a class suitable for the specified save format.<br>(Inherited from [SaveOptions](../saveoptions/)) |
|[ create_save_options(file_name)](../saveoptions/create_save_options/#str) | Creates a save options object of a class suitable for the file extension specified in the given file name.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Examples

Shows how to convert a whole document to PDF with three levels in the document outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert headings of levels 1 to 5.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 1.2.2.1')
builder.writeln('Heading 1.2.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.2.2.2.1')
builder.writeln('Heading 1.2.2.2.2')
# Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()
# The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
# Clicking on an entry in this outline will take us to the location of its respective heading.
# Set the "HeadingsOutlineLevels" property to "4" to exclude all headings whose levels are above 4 from the outline.
options.outline_options.headings_outline_levels = 4
# If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
# an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
# In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
# the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
# In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
# Set the "ExpandedOutlineLevels" property to "2" to automatically expand all heading level 2 and lower outline entries
# and collapse all level and 3 and higher entries when we open the document.
options.outline_options.expanded_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExpandedOutlineLevels.pdf', save_options=options)
```

Shows how to apply text compression when saving a document to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 100:
    builder.writeln('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
    i += 1
# Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()
# Set the "TextCompression" property to "PdfTextCompression.None" to not apply any
# compression to text when we save the document to PDF.
# Set the "TextCompression" property to "PdfTextCompression.Flate" to apply ZIP compression
# to text when we save the document to PDF. The larger the document, the bigger the impact that this will have.
options.text_compression = pdf_text_compression
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.TextCompression.pdf', save_options=options)
```

Shows how to change image color with saving options property.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
# Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
# to modify how that method converts the document to .PDF.
# Set the "ColorMode" property to "Grayscale" to render all images from the document in black and white.
# The size of the output document may be larger with this setting.
# Set the "ColorMode" property to "Normal" to render all images in color.
pdf_save_options = aw.saving.PdfSaveOptions()
pdf_save_options.color_mode = color_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ColorRendering.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)
* class [FixedPageSaveOptions](../fixedpagesaveoptions/)

