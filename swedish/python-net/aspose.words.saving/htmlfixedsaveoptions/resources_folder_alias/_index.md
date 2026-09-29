---
title: HtmlFixedSaveOptions.resources_folder_alias property
linktitle: resources_folder_alias property
articleTitle: resources_folder_alias property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.resources_folder_alias property. Specifies the name of the folder used to construct image URIs written into an Html document"
type: docs
weight: 170
url: /sv/python-net/aspose.words.saving/htmlfixedsaveoptions/resources_folder_alias/
---

## HtmlFixedSaveOptions.resources_folder_alias property

Specifies the name of the folder used to construct image URIs written into an Html document.
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

When you save a [Document](../../../aspose.words/document/) in Html format, Aspose.Words needs to save all
images embedded in the document as standalone files. [HtmlFixedSaveOptions.resources_folder](../resources_folder/)
allows you to specify where the images will be saved and [HtmlFixedSaveOptions.resources_folder_alias](./)
allows to specify how the image URIs will be constructed.




### Examples

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML (ResourceUriPrinter).

```python
class ResourceUriPrinter(aw.saving.IResourceSavingCallback):

    def __init__(self):
        self.m_saved_resource_count = None
        self.m_text = []

    def resource_saving(self, args):
        # Om vi sätter ett mappalias i SaveOptions-objektet kommer vi kunna skriva ut det härifrån.
        self.m_saved_resource_count += 1
        self.m_text.append(f'Resource #{self.m_saved_resource_count} "{args.resource_file_name}"')
        extension = Path(args.resource_file_name).suffix
        if extension in ('.ttf', '.woff'):
            # Som standard använder 'ResourceFileUri' systemmappen för teckensnitt.
            # För att undvika problem på andra plattformar måste du explicit ange sökvägen för teckensnitten.
            args.resource_file_uri = str(Path(ARTIFACTS_DIR) / args.resource_file_name)
        self.m_text.append('\t' + args.resource_file_uri + '\n')
        # Om vi har specificerat en mapp i egenskapen "ResourcesFolderAlias",
        # behöver vi också omdirigera varje ström för att placera dess resurs i den mappen.
        args.resource_stream = system_helper.io.FileStream(args.resource_file_uri, system_helper.io.FileMode.CREATE)
        args.keep_resource_stream_open = False

    def get_text(self):
        return str.join('', self.m_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)
* property [HtmlFixedSaveOptions.resources_folder](../resources_folder/)

