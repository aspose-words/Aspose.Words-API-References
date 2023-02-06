---
title: HtmlSaveOptions class
second_title: Aspose.Words for Python via .NET API Reference
description: "Can be used to specify additional options when saving a document into the [SaveFormat.HTML](../../aspose.words/saveformat/#HTML), [SaveFormat.MHTML](../../aspose.words/saveformat/#MHTML), [SaveFormat.EPUB](../../aspose.words/saveformat/#EPUB) or [SaveFormat.AZW3](../../aspose.words/saveformat/#AZW3) format"
type: docs
weight: 260
url: /python-net/aspose.words.saving/htmlsaveoptions/
---

## HtmlSaveOptions class

Can be used to specify additional options when saving a document into the
[SaveFormat.HTML](../../aspose.words/saveformat/#HTML), [SaveFormat.MHTML](../../aspose.words/saveformat/#MHTML),
[SaveFormat.EPUB](../../aspose.words/saveformat/#EPUB) or [SaveFormat.AZW3](../../aspose.words/saveformat/#AZW3) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/python-net/specify-save-options/) documentation article.




**Inheritance:** [HtmlSaveOptions](./) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [HtmlSaveOptions()](./__init__/#default) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.HTML](../../aspose.words/saveformat/#HTML) format. |
| [HtmlSaveOptions(save_format)](./__init__/#saveformat) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.HTML](../../aspose.words/saveformat/#HTML), [SaveFormat.MHTML](../../aspose.words/saveformat/#MHTML), [SaveFormat.EPUB](../../aspose.words/saveformat/#EPUB) or [SaveFormat.AZW3](../../aspose.words/saveformat/#AZW3) format. |

### Properties

| Name | Description |
| --- | --- |
| [allow_embedding_post_script_fonts](../saveoptions/allow_embedding_post_script_fonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [allow_negative_indent](./allow_negative_indent/) | Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB. Default value is ``False``. |
| [css_class_name_prefix](./css_class_name_prefix/) | Specifies a prefix which is added to all CSS class names. Default value is an empty string and generated CSS class names have no common prefix. |
| [css_saving_callback](./css_saving_callback/) | Allows to control how CSS styles are saved when a document is saved to HTML, MHTML or EPUB. |
| [css_style_sheet_file_name](./css_style_sheet_file_name/) | Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML. Default is an empty string. |
| [css_style_sheet_type](./css_style_sheet_type/) | Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. Default value is [CssStyleSheetType.INLINE](../cssstylesheettype/#INLINE) for HTML/MHTML and  [CssStyleSheetType.EXTERNAL](../cssstylesheettype/#EXTERNAL) for EPUB. |
| [default_template](../saveoptions/default_template/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** (System.String.Empty).<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_3d_effects_rendering_mode](../saveoptions/dml_3d_effects_rendering_mode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_effects_rendering_mode](../saveoptions/dml_effects_rendering_mode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_rendering_mode](../saveoptions/dml_rendering_mode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [document_part_saving_callback](./document_part_saving_callback/) | Allows to control how document parts are saved when a document is saved to HTML or EPUB. |
| [document_split_criteria](./document_split_criteria/) | Specifies how the document should be split when saving to [SaveFormat.HTML](../../aspose.words/saveformat/#HTML), [SaveFormat.EPUB](../../aspose.words/saveformat/#EPUB) or [SaveFormat.AZW3](../../aspose.words/saveformat/#AZW3) format.  Default is [DocumentSplitCriteria.NONE](../documentsplitcriteria/#NONE) for HTML and  [DocumentSplitCriteria.HEADING_PARAGRAPH](../documentsplitcriteria/#HEADING_PARAGRAPH) for EPUB and AZW3. |
| [document_split_heading_level](./document_split_heading_level/) | Specifies the maximum level of headings at which to split the document. Default value is ``2``. |
| [encoding](./encoding/) | Specifies the encoding to use when exporting to HTML, MHTML or EPUB. Default value is ``new UTF8Encoding(false)`` (UTF-8 without BOM). |
| [epub_navigation_map_level](./epub_navigation_map_level/) | Specifies the maximum level of headings populated to the navigation map when exporting to IDPF EPUB or AZW3 formats. Default value is ``3``. |
| [export_cid_urls_for_mhtml_resources](./export_cid_urls_for_mhtml_resources/) | Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. Default value is ``False``. |
| [export_document_properties](./export_document_properties/) | Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB. Default value is ``False``. |
| [export_drop_down_form_field_as_text](./export_drop_down_form_field_as_text/) | Controls how drop-down form fields are saved to HTML or MHTML. Default value is ``False``. |
| [export_font_resources](./export_font_resources/) | Specifies whether font resources should be exported to HTML, MHTML or EPUB. Default is ``False``. |
| [export_fonts_as_base64](./export_fonts_as_base64/) | Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is ``False``. |
| [export_generator_name](../saveoptions/export_generator_name/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [export_headers_footers_mode](./export_headers_footers_mode/) | Specifies how headers and footers are output to HTML, MHTML or EPUB.  Default value is [ExportHeadersFootersMode.PER_SECTION](../exportheadersfootersmode/#PER_SECTION) for HTML/MHTML  and [ExportHeadersFootersMode.NONE](../exportheadersfootersmode/#NONE) for EPUB. |
| [export_images_as_base64](./export_images_as_base64/) | Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. Default is ``False``. |
| [export_language_information](./export_language_information/) | Specifies whether language information is exported to HTML, MHTML or EPUB. Default is ``False``. |
| [export_list_labels](./export_list_labels/) | Controls how list labels are output to HTML, MHTML or EPUB.  Default value is [ExportListLabels.AUTO](../exportlistlabels/#AUTO). |
| [export_original_url_for_linked_images](./export_original_url_for_linked_images/) | Specifies whether original URL should be used as the URL of the linked images. Default value is ``False``. |
| [export_page_margins](./export_page_margins/) | Specifies whether page margins is exported to HTML, MHTML or EPUB. Default is ``False``. |
| [export_page_setup](./export_page_setup/) | Specifies whether page setup is exported to HTML, MHTML or EPUB. Default is ``False``. |
| [export_relative_font_size](./export_relative_font_size/) | Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. Default is ``False``. |
| [export_roundtrip_information](./export_roundtrip_information/) | Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. Default value is ``True`` for HTML and ``False`` for MHTML and EPUB. |
| [export_shapes_as_svg](./export_shapes_as_svg/) | Controls whether [Shape](../../aspose.words.drawing/shape/) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. Default value is ``False``. |
| [export_text_input_form_field_as_text](./export_text_input_form_field_as_text/) | Controls how text input form fields are saved to HTML or MHTML. Default value is ``False``. |
| [export_toc_page_numbers](./export_toc_page_numbers/) | Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. Default value is ``False``. |
| [export_xhtml_transitional](./export_xhtml_transitional/) | Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML. When ``True``, writes a DOCTYPE declaration in the document prior to the root element.  Default value is ``False``. When saving to EPUB or HTML5 ([HtmlVersion.HTML5](../htmlversion/#HTML5)) the DOCTYPE declaration is always written. |
| [font_resources_subsetting_size_threshold](./font_resources_subsetting_size_threshold/) | Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. Default is ``0``. |
| [font_saving_callback](./font_saving_callback/) | Allows to control how fonts are saved when a document is saved to HTML, MHTML or EPUB. |
| [fonts_folder](./fonts_folder/) | Specifies the physical folder where fonts are saved when exporting a document to HTML. Default is an empty string. |
| [fonts_folder_alias](./fonts_folder_alias/) | Specifies the name of the folder used to construct font URIs written into an HTML document. Default is an empty string. |
| [html_version](./html_version/) | Specifies version of HTML standard that should be used when saving the document to HTML or MHTML. Default value is [HtmlVersion.XHTML](../htmlversion/#XHTML). |
| [image_resolution](./image_resolution/) | Specifies the output resolution for images when exporting to HTML, MHTML or EPUB. Default is ``96 dpi``. |
| [image_saving_callback](./image_saving_callback/) | Allows to control how images are saved when a document is saved to HTML, MHTML or EPUB. |
| [images_folder](./images_folder/) | Specifies the physical folder where images are saved when exporting a document to HTML format. Default is an empty string. |
| [images_folder_alias](./images_folder_alias/) | Specifies the name of the folder used to construct image URIs written into an HTML document. Default is an empty string. |
| [iml_rendering_mode](../saveoptions/iml_rendering_mode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [memory_optimization](../saveoptions/memory_optimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [metafile_format](./metafile_format/) | Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB. Default value is [HtmlMetafileFormat.PNG](../htmlmetafileformat/#PNG), meaning that metafiles are rendered to raster PNG images. |
| [office_math_output_mode](./office_math_output_mode/) | Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. Default value is [HtmlOfficeMathOutputMode.IMAGE](../htmlofficemathoutputmode/#IMAGE). |
| [pretty_format](../saveoptions/pretty_format/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progress_callback](../saveoptions/progress_callback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [resolve_font_names](./resolve_font_names/) | Specifies whether font family names used in the document are resolved and substituted according to [Document.font_settings](../../aspose.words/document/font_settings/) when being written into HTML-based formats. |
| [resource_folder](./resource_folder/) | Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML. Default is an empty string. |
| [resource_folder_alias](./resource_folder_alias/) | Specifies the name of the folder used to construct URIs of all resources written into an HTML document. Default is an empty string. |
| [save_format](./save_format/) | Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.HTML](../../aspose.words/saveformat/#HTML), [SaveFormat.MHTML](../../aspose.words/saveformat/#MHTML), [SaveFormat.EPUB](../../aspose.words/saveformat/#EPUB) or [SaveFormat.AZW3](../../aspose.words/saveformat/#AZW3). |
| [scale_image_to_shape_size](./scale_image_to_shape_size/) | Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. Default value is ``True``. |
| [table_width_output_mode](./table_width_output_mode/) | Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. Default value is [HtmlElementSizeOutputMode.ALL](../htmlelementsizeoutputmode/#ALL). |
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

Shows how to specify the folder for storing linked images after saving to .html.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

images_dir = os.path.join(ARTIFACTS_DIR, "SaveHtmlWithOptions")

if os.path.exists(images_dir):
    shutil.rmtree(images_dir)

os.makedirs(images_dir)

# Set an option to export form fields as plain text instead of HTML input elements.
options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
options.export_text_input_form_field_as_text = True
options.images_folder = images_dir

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.image_folder.html", options)
```

### See Also

* module [aspose.words.saving](../)
* class [SaveOptions](../saveoptions/)

