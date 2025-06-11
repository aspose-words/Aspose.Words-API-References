---
title: XamlFixedSaveOptions class
linktitle: XamlFixedSaveOptions class
articleTitle: XamlFixedSaveOptions class
second_title: Aspose.Words for Python
description: "aspose.words.saving.XamlFixedSaveOptions class. Can be used to specify additional options when saving a document into the [SaveFormat.XAML_FIXED](../../aspose.words/saveformat/#XAML_FIXED) format"
type: docs
weight: 910
url: /python-net/aspose.words.saving/xamlfixedsaveoptions/
---

## XamlFixedSaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.XAML_FIXED](../../aspose.words/saveformat/#XAML_FIXED) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/python-net/specify-save-options/) documentation article.




**Inheritance:** [XamlFixedSaveOptions](./) → [FixedPageSaveOptions](../fixedpagesaveoptions/) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [XamlFixedSaveOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [allow_embedding_post_script_fonts](../saveoptions/allow_embedding_post_script_fonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [color_mode](../fixedpagesaveoptions/color_mode/) | Gets or sets a value determining how colors are rendered.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [default_template](../saveoptions/default_template/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_3d_effects_rendering_mode](../saveoptions/dml_3d_effects_rendering_mode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_effects_rendering_mode](../saveoptions/dml_effects_rendering_mode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_rendering_mode](../saveoptions/dml_rendering_mode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [export_generator_name](../saveoptions/export_generator_name/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
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
| [resource_saving_callback](./resource_saving_callback/) | Allows to control how resources (images and fonts) are saved when a document is exported to fixed page Xaml format. |
| [resources_folder](./resources_folder/) | Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format. Default is ``None``. |
| [resources_folder_alias](./resources_folder_alias/) | Specifies the name of the folder used to construct image URIs written into an fixed page Xaml document. Default is ``None``. |
| [save_format](./save_format/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.XAML_FIXED](../../aspose.words/saveformat/#XAML_FIXED). |
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

Shows how to print the URIs of linked resources created while converting a document to fixed-form .xaml.

```python
def test_resource_folder(self):

    doc = aw.Document(MY_DIR + "Rendering.docx")
    callback = ExXamlFixedSaveOptions.ResourceUriPrinter()

    # Create a "XamlFixedSaveOptions" object, which we can pass to the document's "save" method
    # to modify how we save the document to the XAML save format.
    options = aw.saving.XamlFixedSaveOptions()

    self.assertEqual(aw.SaveFormat.XAML_FIXED, options.save_format)

    # Use the "resources_folder" property to assign a folder in the local file system into which
    # Aspose.Words will save all the document's linked resources, such as images and fonts.
    options.resources_folder = ARTIFACTS_DIR + "XamlFixedResourceFolder"

    # Use the "resources_folder_alias" property to use this folder
    # when constructing image URIs instead of the resources folder's name.
    options.resources_folder_alias = ARTIFACTS_DIR + "XamlFixedFolderAlias"

    options.resource_saving_callback = callback

    # A folder specified by "resources_folder_alias" will need to contain the resources instead of "resources_folder".
    # We must ensure the folder exists before the callback's streams can put their resources into it.
    os.makedirs(options.resources_folder_alias)

    doc.save(ARTIFACTS_DIR + "XamlFixedSaveOptions.resource_folder.xaml", options)

    for resource in callback.resources:
        print(resource)


class ResourceUriPrinter(aw.saving.IResourceSavingCallback):
    """Counts and prints URIs of resources created during conversion to fixed .xaml."""

    def __init__(self):

        self.resources = [] # type: List[str]

    def resource_saving(self, args: aw.saving.ResourceSavingArgs):

        self.resources.add(f"Resource \"{args.resource_file_name}\"\n\t{args.resource_file_uri}")

        # If we specified a resource folder alias, we would also need
        # to redirect each stream to put its resource in the alias folder.
        args.resource_stream = open(args.resource_file_uri, 'wb')
        args.keep_resource_stream_open = False
```

### See Also

* module [aspose.words.saving](../)
* class [FixedPageSaveOptions](../fixedpagesaveoptions/)

