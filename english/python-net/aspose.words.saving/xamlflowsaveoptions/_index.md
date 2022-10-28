---
title: XamlFlowSaveOptions class
second_title: Aspose.Words for Python via .NET API Reference
description: "Can be used to specify additional options when saving a document into the  [SaveFormat.XAML_FLOW](../../aspose.words/saveformat/#XAML_FLOW) or [SaveFormat.XAML_FLOW_PACK](../../aspose.words/saveformat/#XAML_FLOW_PACK) format"
type: docs
weight: 830
url: /python-net/aspose.words.saving/xamlflowsaveoptions/
---

## XamlFlowSaveOptions class

Can be used to specify additional options when saving a document into the 
[SaveFormat.XAML_FLOW](../../aspose.words/saveformat/#XAML_FLOW) or [SaveFormat.XAML_FLOW_PACK](../../aspose.words/saveformat/#XAML_FLOW_PACK) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/net/specify-save-options/) documentation article.




**Inheritance:** [XamlFlowSaveOptions](./) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [XamlFlowSaveOptions()](./__init__/#default) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.XAML_FLOW](../../aspose.words/saveformat/#XAML_FLOW) format. |
| [XamlFlowSaveOptions(save_format)](./__init__/#saveformat) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.XAML_FLOW](../../aspose.words/saveformat/#XAML_FLOW) or [SaveFormat.XAML_FLOW_PACK](../../aspose.words/saveformat/#XAML_FLOW_PACK) format. |

### Properties

| Name | Description |
| --- | --- |
| [allow_embedding_post_script_fonts](../saveoptions/allow_embedding_post_script_fonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [default_template](../saveoptions/default_template/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** (System.String.Empty).<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_3d_effects_rendering_mode](../saveoptions/dml_3d_effects_rendering_mode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_effects_rendering_mode](../saveoptions/dml_effects_rendering_mode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_rendering_mode](../saveoptions/dml_rendering_mode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [export_generator_name](../saveoptions/export_generator_name/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [image_saving_callback](./image_saving_callback/) | Allows to control how images are saved when a document is saved to XAML. |
| [images_folder](./images_folder/) | Specifies the physical folder where images are saved when exporting a document to XAML format. Default is an empty string. |
| [images_folder_alias](./images_folder_alias/) | Specifies the name of the folder used to construct image URIs written into an XAML document. Default is an empty string. |
| [iml_rendering_mode](../saveoptions/iml_rendering_mode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [memory_optimization](../saveoptions/memory_optimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [pretty_format](../saveoptions/pretty_format/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progress_callback](../saveoptions/progress_callback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [save_format](./save_format/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.XAML_FLOW](../../aspose.words/saveformat/#XAML_FLOW). |
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

Shows how to print the filenames of linked images created while converting a document to flow-form .xaml.

```python
def test_image_folder(self):

    doc = aw.Document(MY_DIR + "Rendering.docx")

    callback = ExXamlFlowSaveOptions.ImageUriPrinter(ARTIFACTS_DIR + "XamlFlowImageFolderAlias")

    # Create a "XamlFlowSaveOptions" object, which we can pass to the document's "save" method
    # to modify how we save the document to the XAML save format.
    options = aw.saving.XamlFlowSaveOptions()

    self.assertEqual(aw.SaveFormat.XAML_FLOW, options.save_format)

    # Use the "images_folder" property to assign a folder in the local file system into which
    # Aspose.Words will save all the document's linked images.
    options.images_folder = ARTIFACTS_DIR + "XamlFlowImageFolder"

    # Use the "images_folder_alias" property to use this folder
    # when constructing image URIs instead of the images folder's name.
    options.images_folder_alias = ARTIFACTS_DIR + "XamlFlowImageFolderAlias"

    options.image_saving_callback = callback

    # A folder specified by "images_folder_alias" will need to contain the resources instead of "images_folder".
    # We must ensure the folder exists before the callback's streams can put their resources into it.
    os.makedirs(options.images_folder_alias)

    doc.save(ARTIFACTS_DIR + "XamlFlowSaveOptions.image_folder.xaml", options)

    for resource in callback.Resources:
        print(f"{callback.images_folder_alias}/{resource}")


class ImageUriPrinter(aw.saving.IImageSavingCallback):
    """Counts and prints filenames of images while their parent document is converted to flow-form .xaml."""

    def __init__(self, images_folder_alias: str):

        self.images_folder_alias = images_folder_alias
        self.resources = [] # type: List[str]

    def image_saving(self, args: aw.saving.ImageSavingArgs):

        self.resources.add(args.image_file_name)

        # If we specified an image folder alias, we would also need
        # to redirect each stream to put its image in the alias folder.
        args.image_stream = open(f"{self.images_folder_alias}/{args.image_file_name}", "wb")
        args.keep_image_stream_open = False
```

### See Also

* module [aspose.words.saving](../)
* class [SaveOptions](../saveoptions/)

