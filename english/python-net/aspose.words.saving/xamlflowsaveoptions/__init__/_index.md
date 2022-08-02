---
title: XamlFlowSaveOptions constructor
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.saving.XamlFlowSaveOptions constructor"
type: docs
weight: 10
url: /python-net/aspose.words.saving/xamlflowsaveoptions/__init__/
---

## XamlFlowSaveOptions() {#default}

Initializes a new instance of this class that can be used to save a document in the [SaveFormat.XAML_FLOW](../../../aspose.words/saveformat/#XAML_FLOW) format.



```python
def __init__(self):
    ...
```

## XamlFlowSaveOptions(save_format) {#saveformat}

Initializes a new instance of this class that can be used to save a document in the [SaveFormat.XAML_FLOW](../../../aspose.words/saveformat/#XAML_FLOW)
or [SaveFormat.XAML_FLOW_PACK](../../../aspose.words/saveformat/#XAML_FLOW_PACK) format.



```python
def __init__(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) |  |

## Examples

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

## See Also

* module [aspose.words.saving](../../)
* class [XamlFlowSaveOptions](../)

