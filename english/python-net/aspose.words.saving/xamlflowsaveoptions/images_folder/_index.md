---
title: images_folder property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the physical folder where images are saved when exporting a document to XAML format"
type: docs
weight: 30
url: /python-net/aspose.words.saving/xamlflowsaveoptions/images_folder/
---

## XamlFlowSaveOptions.images_folder property

Specifies the physical folder where images are saved when exporting a document to XAML format.
Default is an empty string.

When you save a [Document](../../../aspose.words/document/) in XAML format, Aspose.Words needs to save all 
images embedded in the document as standalone files. [XamlFlowSaveOptions.images_folder](./) 
allows you to specify where the images will be saved and [XamlFlowSaveOptions.images_folder_alias](../images_folder_alias/) 
allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the 
images in the same folder where the document file is saved. Use [XamlFlowSaveOptions.images_folder](./)
to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, 
but still needs to save the images somewhere. In this case, you need to specify an accessible folder 
in the [XamlFlowSaveOptions.images_folder](./) property or provide custom streams via 
the [XamlFlowSaveOptions.image_saving_callback](../image_saving_callback/) event handler.




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

* module [aspose.words.saving](../../)
* class [XamlFlowSaveOptions](../)
* property [XamlFlowSaveOptions.images_folder_alias](../images_folder_alias/)
* property [XamlFlowSaveOptions.image_saving_callback](../image_saving_callback/)

