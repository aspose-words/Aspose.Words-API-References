---
title: SvgSaveOptions.resources_folder property
linktitle: resources_folder property
articleTitle: resources_folder property
second_title: Aspose.Words for Python
description: "SvgSaveOptions.resources_folder property. Specifies the physical folder where resources (images) are saved when exporting a document to Svg format"
type: docs
weight: 50
url: /python-net/aspose.words.saving/svgsaveoptions/resources_folder/
---

## SvgSaveOptions.resources_folder property

Specifies the physical folder where resources (images) are saved when exporting a document to Svg format.
Default is ``None``.


Has effect only if [SvgSaveOptions.export_embedded_images](../export_embedded_images/) property is ``False``.

When you save a [Document](../../../aspose.words/document/) in SVG format, Aspose.Words needs to save all 
images embedded in the document as standalone files. [SvgSaveOptions.resources_folder](./) 
allows you to specify where the images will be saved and [SvgSaveOptions.resources_folder_alias](../resources_folder_alias/) 
allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the 
images in the same folder where the document file is saved. Use [SvgSaveOptions.resources_folder](./)
to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, 
but still needs to save the images somewhere. In this case, you need to specify an accessible folder 
in the [SvgSaveOptions.resources_folder](./) property




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

* module [aspose.words.saving](../../)
* class [SvgSaveOptions](../)
* property [SvgSaveOptions.resources_folder_alias](../resources_folder_alias/)

