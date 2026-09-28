---
title: IResourceSavingCallback.resource_saving method
linktitle: resource_saving method
articleTitle: resource_saving method
second_title: Aspose.Words for Python
description: "IResourceSavingCallback.resource_saving method. Called when Aspose.Words saves an external resource to fixed page HTML or SVG formats."
type: docs
weight: 10
url: /ar/python-net/aspose.words.saving/iresourcesavingcallback/resource_saving/
---

## resource_saving(args) {#resourcesavingargs}

Called when Aspose.Words saves an external resource to fixed page HTML or SVG formats.


```python
def resource_saving(self, args: aspose.words.saving.ResourceSavingArgs):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| args | [ResourceSavingArgs](../../resourcesavingargs/) |  |

### Examples

Shows how to use a callback to track external resources created while converting a document to HTML (FontSavingCallback).

```python
class FontSavingCallback(aw.saving.IResourceSavingCallback):

    def __init__(self):
        self.m_text = []

    def resource_saving(self, args):
        self.m_text.append(f'Original document URI:\t{args.document.original_file_name}' + '\n')
        self.m_text.append(f'Resource being saved:\t{args.resource_file_name}' + '\n')
        self.m_text.append(f'Full uri after saving:\t{args.resource_file_uri}\n' + '\n')

    def get_text(self):
        return str.join('', self.m_text)
```

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML (ResourceUriPrinter).

```python
class ResourceUriPrinter(aw.saving.IResourceSavingCallback):

    def __init__(self):
        self.m_saved_resource_count = None
        self.m_text = []

    def resource_saving(self, args):
        # إذا قمنا بتعيين اسم مستعار للمجلد في كائن SaveOptions، سنتمكن من طباعته من هنا.
        self.m_saved_resource_count += 1
        self.m_text.append(f'Resource #{self.m_saved_resource_count} "{args.resource_file_name}"')
        extension = Path(args.resource_file_name).suffix
        if extension in ('.ttf', '.woff'):
            # بشكل افتراضي، يستخدم 'ResourceFileUri' مجلد النظام للخطوط.
            # لتجنب المشكلات في المنصات الأخرى يجب عليك تحديد مسار الخطوط صراحةً.
            args.resource_file_uri = str(Path(ARTIFACTS_DIR) / args.resource_file_name)
        self.m_text.append('\t' + args.resource_file_uri + '\n')
        # إذا كنا قد حددنا مجلدًا في خاصية "ResourcesFolderAlias"،
        # سنحتاج أيضًا إلى إعادة توجيه كل تدفق لوضع موارده في ذلك المجلد.
        args.resource_stream = system_helper.io.FileStream(args.resource_file_uri, system_helper.io.FileMode.CREATE)
        args.keep_resource_stream_open = False

    def get_text(self):
        return str.join('', self.m_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [IResourceSavingCallback](../)

