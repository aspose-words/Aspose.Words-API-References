---
title: HtmlFixedSaveOptions.resources_folder_alias property
linktitle: resources_folder_alias property
articleTitle: resources_folder_alias property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.resources_folder_alias property. Specifies the name of the folder used to construct image URIs written into an Html document"
type: docs
weight: 170
url: /zh/python-net/aspose.words.saving/htmlfixedsaveoptions/resources_folder_alias/
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
* property [HtmlFixedSaveOptions.resources_folder](../resources_folder/)

