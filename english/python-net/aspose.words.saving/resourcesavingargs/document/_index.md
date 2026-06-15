---
title: ResourceSavingArgs.document property
linktitle: document property
articleTitle: document property
second_title: Aspose.Words for Python
description: "ResourceSavingArgs.document property. Gets the document object that is currently being saved."
type: docs
weight: 10
url: /python-net/aspose.words.saving/resourcesavingargs/document/
---

## ResourceSavingArgs.document property

Gets the document object that is currently being saved.


```python
@property
def document(self) -> aspose.words.Document:
    ...

```

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

### See Also

* module [aspose.words.saving](../../)
* class [ResourceSavingArgs](../)

