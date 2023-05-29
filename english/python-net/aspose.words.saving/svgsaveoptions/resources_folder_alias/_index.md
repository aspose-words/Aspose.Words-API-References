---
title: SvgSaveOptions.resources_folder_alias property
linktitle: resources_folder_alias property
articleTitle: resources_folder_alias property
second_title: Aspose.Words for Python
description: "SvgSaveOptions.resources_folder_alias property. Specifies the name of the folder used to construct image URIs written into an SVG document"
type: docs
weight: 60
url: /python-net/aspose.words.saving/svgsaveoptions/resources_folder_alias/
---

## SvgSaveOptions.resources_folder_alias property

Specifies the name of the folder used to construct image URIs written into an SVG document.
Default is ``None``.


When you save a [Document](../../../aspose.words/document/) in SVG format, Aspose.Words needs to save all 
images embedded in the document as standalone files. [SvgSaveOptions.resources_folder](../resources_folder/) 
allows you to specify where the images will be saved and [SvgSaveOptions.resources_folder_alias](./) 
allows to specify how the image URIs will be constructed.




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
* property [SvgSaveOptions.resources_folder](../resources_folder/)

