---
title: HtmlFixedSaveOptions.show_page_border property
linktitle: show_page_border property
articleTitle: show_page_border property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.show_page_border property. Specifies whether border around pages should be shown"
type: docs
weight: 200
url: /sv/python-net/aspose.words.saving/htmlfixedsaveoptions/show_page_border/
---

## HtmlFixedSaveOptions.show_page_border property

Specifies whether border around pages should be shown.
Default is ``True``.



```python
@property
def show_page_border(self) -> bool:
    ...

@show_page_border.setter
def show_page_border(self, value: bool):
    ...

```

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

