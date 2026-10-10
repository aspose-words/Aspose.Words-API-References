---
title: HtmlFixedSaveOptions.show_page_border property
linktitle: show_page_border property
articleTitle: show_page_border property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.show_page_border property. Specifies whether border around pages should be shown"
type: docs
weight: 200
url: /zh/python-net/aspose.words.saving/htmlfixedsaveoptions/show_page_border/
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
        # 如果我们在 SaveOptions 对象中设置文件夹别名，我们就可以从这里打印它。
        self.m_saved_resource_count += 1
        self.m_text.append(f'Resource #{self.m_saved_resource_count} "{args.resource_file_name}"')
        extension = Path(args.resource_file_name).suffix
        if extension in ('.ttf', '.woff'):
            # 默认情况下，'ResourceFileUri' 使用系统文件夹存放字体。
            # 为避免在其他平台出现问题，您必须显式指定字体的路径。
            args.resource_file_uri = str(Path(ARTIFACTS_DIR) / args.resource_file_name)
        self.m_text.append('\t' + args.resource_file_uri + '\n')
        # 如果我们在 "ResourcesFolderAlias" 属性中指定了文件夹，
        # 我们还需要重定向每个流，将其资源放入该文件夹。
        args.resource_stream = system_helper.io.FileStream(args.resource_file_uri, system_helper.io.FileMode.CREATE)
        args.keep_resource_stream_open = False

    def get_text(self):
        return str.join('', self.m_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

