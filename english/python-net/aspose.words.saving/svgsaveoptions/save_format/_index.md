---
title: SvgSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "SvgSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 100
url: /python-net/aspose.words.saving/svgsaveoptions/save_format/
---

## SvgSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.SVG](../../../aspose.words/saveformat/#SVG).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
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

