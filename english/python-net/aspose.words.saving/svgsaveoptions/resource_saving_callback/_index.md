---
title: SvgSaveOptions.resource_saving_callback property
linktitle: resource_saving_callback property
articleTitle: resource_saving_callback property
second_title: Aspose.Words for Python
description: "SvgSaveOptions.resource_saving_callback property. Allows to control how resources (images) are saved when a document is exported to SVG format."
type: docs
weight: 70
url: /python-net/aspose.words.saving/svgsaveoptions/resource_saving_callback/
---

## SvgSaveOptions.resource_saving_callback property

Allows to control how resources (images) are saved when a document is exported to SVG format.


```python
@property
def resource_saving_callback(self) -> aspose.words.saving.IResourceSavingCallback:
    ...

@resource_saving_callback.setter
def resource_saving_callback(self, value: aspose.words.saving.IResourceSavingCallback):
    ...

```

### Examples

Shows how to manipulate and print the URIs of linked resources created while converting a document to .svg.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
options = aw.saving.SvgSaveOptions()
options.save_format = aw.SaveFormat.SVG
options.export_embedded_images = False
options.resources_folder = ARTIFACTS_DIR + 'SvgResourceFolder'
options.resources_folder_alias = ARTIFACTS_DIR + 'SvgResourceFolderAlias'
options.show_page_border = False
options.resource_saving_callback = self.ResourceUriPrinter()
system_helper.io.Directory.create_directory(options.resources_folder_alias)
doc.save(file_name=ARTIFACTS_DIR + 'SvgSaveOptions.SvgResourceFolder.svg', save_options=options)
```

Shows how to manipulate and print the URIs of linked resources created while converting a document to .svg (ResourceUriPrinter).

```python
class ResourceUriPrinter(aw.saving.IResourceSavingCallback):

    def __init__(self):
        self.m_saved_resource_count = None

    def resource_saving(self, args):
        mSavedResourceCount = 0
        mSavedResourceCount += 1
        print(f'Resource #{mSavedResourceCount} "{args.resource_file_name}"')
        print('\t' + args.resource_file_uri)
```

### See Also

* module [aspose.words.saving](../../)
* class [SvgSaveOptions](../)

