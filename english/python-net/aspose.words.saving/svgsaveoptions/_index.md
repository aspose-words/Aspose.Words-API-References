---
title: SvgSaveOptions class
second_title: Aspose.Words for Python via .NET API Reference
description: "Can be used to specify additional options when saving a document into the [SaveFormat.SVG](../../aspose.words/saveformat/#SVG) format."
type: docs
weight: 730
url: /python-net/aspose.words.saving/svgsaveoptions/
---

## SvgSaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.SVG](../../aspose.words/saveformat/#SVG) format.



**Inheritance:** [SvgSaveOptions](./) → [FixedPageSaveOptions](../fixedpagesaveoptions/) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [SvgSaveOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [allow_embedding_post_script_fonts](../saveoptions/allow_embedding_post_script_fonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [color_mode](../fixedpagesaveoptions/color_mode/) | Gets or sets a value determining how colors are rendered.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [default_template](../saveoptions/default_template/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** (System.String.Empty).<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_3d_effects_rendering_mode](../saveoptions/dml_3d_effects_rendering_mode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_effects_rendering_mode](../saveoptions/dml_effects_rendering_mode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_rendering_mode](../saveoptions/dml_rendering_mode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [export_embedded_images](./export_embedded_images/) | Specified whether images should be embedded into SVG document as base64. Note setting this flag can significantly increase size of output SVG file. |
| [export_generator_name](../saveoptions/export_generator_name/) | When true, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [fit_to_view_port](./fit_to_view_port/) | Specifies if the output SVG should fill the available viewport area (browser window or container). When set to true width and height of output SVG are set to 100%. |
| [flat_opc_xml_mapping_only](../saveoptions/flat_opc_xml_mapping_only/) | Gets or sets value determining which document formats are allowed to be mapped by [StructuredDocumentTag.xml_mapping](../../aspose.words.markup/structureddocumenttag/xml_mapping/). By default only [LoadFormat.FLAT_OPC](../../aspose.words/loadformat/#FLAT_OPC) document format is allowed to be mapped.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [iml_rendering_mode](../saveoptions/iml_rendering_mode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [jpeg_quality](../fixedpagesaveoptions/jpeg_quality/) | Gets or sets a value determining the quality of the JPEG images inside Html document.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [memory_optimization](../saveoptions/memory_optimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [metafile_rendering_options](../fixedpagesaveoptions/metafile_rendering_options/) | Allows to specify metafile rendering options.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [numeral_format](../fixedpagesaveoptions/numeral_format/) | Gets or sets [NumeralFormat](../numeralformat/) used for rendering of numerals. European numerals are used by default.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [optimize_output](../fixedpagesaveoptions/optimize_output/) | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to true.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [page_saving_callback](../fixedpagesaveoptions/page_saving_callback/) | Allows to control how separate pages are saved when a document is exported to fixed page format.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [page_set](../fixedpagesaveoptions/page_set/) | Gets or sets the pages to render. Default is all the pages in the document.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [pretty_format](../saveoptions/pretty_format/) | When ``true``, pretty formats output where applicable.  Default value is **false**.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progress_callback](../saveoptions/progress_callback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [resource_saving_callback](./resource_saving_callback/) | Allows to control how resources (images) are saved when a document is exported to SVG format. |
| [resources_folder](./resources_folder/) | Specifies the physical folder where resources (images) are saved when exporting a document to Svg format. Default is ``null``. |
| [resources_folder_alias](./resources_folder_alias/) | Specifies the name of the folder used to construct image URIs written into an SVG document. Default is ``null``. |
| [save_format](./save_format/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.SVG](../../aspose.words/saveformat/#SVG). |
| [show_page_border](./show_page_border/) | Controls whether a border is added to the outline of the page. Default is ``true``. |
| [temp_folder](../saveoptions/temp_folder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``null`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [text_output_mode](./text_output_mode/) | Gets or sets a value determining how text should be rendered in SVG. |
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

Shows how to manipulate and print the URIs of linked resources created while converting a document to .svg.

```python
#def test_svg_resource_folder(self):

#    doc = aw.Document(MY_DIR + "Rendering.docx")

#    options = aw.saving.SvgSaveOptions()
#    options.save_format = aw.saving.SaveFormat.SVG
#    options.export_embedded_images = False
#    options.resources_folder = ARTIFACTS_DIR + "SvgResourceFolder"
#    options.resources_folder_alias = ARTIFACTS_DIR + "SvgResourceFolderAlias",
#    options.show_page_border = False
#    options.resource_saving_callback = ExSvgSaveOptions.ResourceUriPrinter()

#    os.mkdir(options.resources_folder_alias)

#    doc.save(ARTIFACTS_DIR + "SvgSaveOptions.SvgResourceFolder.svg", options)

#class ResourceUriPrinter(aw.saving.IResourceSavingCallback):
#    """Counts and prints URIs of resources contained by as they are converted to .svg."""

#    def __init__(self):
#        self.saved_resource_count = 0

#    def resource_saving(self, args: aw.saving.ResourceSavingArgs):
#        self.saved_resource_count += 1
#        print(f"Resource #{self.saved_resource_count} \"{args.resource_file_name}\"")
#        print("\t" + args.resource_file_uri)
```

### See Also

* module [aspose.words.saving](../)
* class [FixedPageSaveOptions](../fixedpagesaveoptions/)

