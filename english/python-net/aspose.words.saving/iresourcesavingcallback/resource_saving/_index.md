---
title: IResourceSavingCallback.resource_saving method
linktitle: resource_saving method
articleTitle: resource_saving method
second_title: Aspose.Words for Python
description: "IResourceSavingCallback.resource_saving method. Called when Aspose.Words saves an external resource to fixed page HTML or SVG formats."
type: docs
weight: 10
url: /python-net/aspose.words.saving/iresourcesavingcallback/resource_saving/
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
        # If we set a folder alias in the SaveOptions object, we will be able to print it from here.
        self.m_saved_resource_count += 1
        self.m_text.append(f'Resource #{self.m_saved_resource_count} "{args.resource_file_name}"')
        extension = Path(args.resource_file_name).suffix
        if extension in ('.ttf', '.woff'):
            # By default, 'ResourceFileUri' uses system folder for fonts.
            # To avoid problems in other platforms you must explicitly specify the path for the fonts.
            args.resource_file_uri = str(Path(ARTIFACTS_DIR) / args.resource_file_name)
        self.m_text.append('\t' + args.resource_file_uri + '\n')
        # If we have specified a folder in the "ResourcesFolderAlias" property,
        # we will also need to redirect each stream to put its resource in that folder.
        args.resource_stream = system_helper.io.FileStream(args.resource_file_uri, system_helper.io.FileMode.CREATE)
        args.keep_resource_stream_open = False

    def get_text(self):
        return str.join('', self.m_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [IResourceSavingCallback](../)

