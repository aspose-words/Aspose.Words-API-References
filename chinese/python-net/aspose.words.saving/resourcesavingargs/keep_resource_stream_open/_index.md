---
title: ResourceSavingArgs.keep_resource_stream_open property
linktitle: keep_resource_stream_open property
articleTitle: keep_resource_stream_open property
second_title: Aspose.Words for Python
description: "ResourceSavingArgs.keep_resource_stream_open property. Specifies whether Aspose.Words should keep the stream open or close it after saving a resource."
type: docs
weight: 20
url: /zh/python-net/aspose.words.saving/resourcesavingargs/keep_resource_stream_open/
---

## ResourceSavingArgs.keep_resource_stream_open property

Specifies whether Aspose.Words should keep the stream open or close it after saving a resource.


```python
@property
def keep_resource_stream_open(self) -> bool:
    ...

@keep_resource_stream_open.setter
def keep_resource_stream_open(self, value: bool):
    ...

```

### Remarks

Default is ``False`` and Aspose.Words will close the stream you provided
in the [ResourceSavingArgs.resource_stream](../resource_stream/) property after writing a resource into it.
Specify ``True`` to keep the stream open.




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
* class [ResourceSavingArgs](../)
* property [ResourceSavingArgs.resource_stream](../resource_stream/)

