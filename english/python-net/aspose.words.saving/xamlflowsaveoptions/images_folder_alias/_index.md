---
title: XamlFlowSaveOptions.images_folder_alias property
linktitle: images_folder_alias property
articleTitle: images_folder_alias property
second_title: Aspose.Words for Python
description: "XamlFlowSaveOptions.images_folder_alias property. Specifies the name of the folder used to construct image URIs written into an XAML document"
type: docs
weight: 40
url: /python-net/aspose.words.saving/xamlflowsaveoptions/images_folder_alias/
---

## XamlFlowSaveOptions.images_folder_alias property

Specifies the name of the folder used to construct image URIs written into an XAML document.
Default is an empty string.


```python
@property
def images_folder_alias(self) -> str:
    ...

@images_folder_alias.setter
def images_folder_alias(self, value: str):
    ...

```

### Remarks

When you save a [Document](../../../aspose.words/document/) in XAML format, Aspose.Words needs to save all 
images embedded in the document as standalone files. [XamlFlowSaveOptions.images_folder](../images_folder/) 
allows you to specify where the images will be saved and [XamlFlowSaveOptions.images_folder_alias](./) 
allows to specify how the image URIs will be constructed.

If [XamlFlowSaveOptions.images_folder_alias](./) is not an empty string, then the image URI written
to XAML will be *ImagesFolderAlias + \<image file name\>*.

If [XamlFlowSaveOptions.images_folder_alias](./) is an empty string, then the image URI written 
to XAML will be *ImagesFolder + \<image file name\>*.

If [XamlFlowSaveOptions.images_folder_alias](./) is set to '.' (dot), then the image file name 
will be written to XAML without path regardless of other options.




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
* property [XamlFlowSaveOptions.images_folder](../images_folder/)
* property [XamlFlowSaveOptions.image_saving_callback](../image_saving_callback/)

