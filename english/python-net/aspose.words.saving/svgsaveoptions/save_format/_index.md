---
title: SvgSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "SvgSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 70
url: /python-net/aspose.words.saving/svgsaveoptions/save_format/
---

## SvgSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.SVG](../../../aspose.words/saveformat/#SVG).



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

