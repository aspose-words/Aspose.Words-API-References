---
title: SvgSaveOptions.resources_folder_alias property
linktitle: resources_folder_alias property
articleTitle: resources_folder_alias property
second_title: Aspose.Words for Python
description: "SvgSaveOptions.resources_folder_alias property. Specifies the name of the folder used to construct image URIs written into an SVG document"
type: docs
weight: 90
url: /python-net/aspose.words.saving/svgsaveoptions/resources_folder_alias/
---

## SvgSaveOptions.resources_folder_alias property

Specifies the name of the folder used to construct image URIs written into an SVG document.
Default is ``None``.



```python
@property
def resources_folder_alias(self) -> str:
    ...

@resources_folder_alias.setter
def resources_folder_alias(self, value: str):
    ...

```

### Remarks

When you save a [Document](../../../aspose.words/document/) in SVG format, Aspose.Words needs to save all
images embedded in the document as standalone files. [SvgSaveOptions.resources_folder](../resources_folder/)
allows you to specify where the images will be saved and [SvgSaveOptions.resources_folder_alias](./)
allows to specify how the image URIs will be constructed.




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
* property [SvgSaveOptions.resources_folder](../resources_folder/)

