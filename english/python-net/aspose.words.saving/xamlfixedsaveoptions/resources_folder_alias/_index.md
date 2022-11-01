---
title: resources_folder_alias property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the name of the folder used to construct image URIs written into an fixed page Xaml document"
type: docs
weight: 40
url: /python-net/aspose.words.saving/xamlfixedsaveoptions/resources_folder_alias/
---

## XamlFixedSaveOptions.resources_folder_alias property

Specifies the name of the folder used to construct image URIs written into an fixed page Xaml document.
Default is ``None``.


When you save a [Document](../../../aspose.words/document/) in fixed page Xaml format, Aspose.Words needs to save all 
images embedded in the document as standalone files. [XamlFixedSaveOptions.resources_folder](../resources_folder/) 
allows you to specify where the images will be saved and [XamlFixedSaveOptions.resources_folder_alias](./) 
allows to specify how the image URIs will be constructed.




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

* module [aspose.words.saving](../../)
* class [XamlFixedSaveOptions](../)
* property [XamlFixedSaveOptions.resources_folder](../resources_folder/)

