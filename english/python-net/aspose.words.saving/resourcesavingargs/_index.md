---
title: ResourceSavingArgs class
linktitle: ResourceSavingArgs class
articleTitle: ResourceSavingArgs class
second_title: Aspose.Words for Python
description: "aspose.words.saving.ResourceSavingArgs class. Provides data for the [IResourceSavingCallback.resource_saving()](../iresourcesavingcallback/resource_saving/#resourcesavingargs) event"
type: docs
weight: 790
url: /python-net/aspose.words.saving/resourcesavingargs/
---

## ResourceSavingArgs class

Provides data for the [IResourceSavingCallback.resource_saving()](../iresourcesavingcallback/resource_saving/#resourcesavingargs) event.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/python-net/save-a-document/) documentation article.




### Remarks

By default, when Aspose.Words saves a document to fixed page HTML, SVG or Markdown, it saves each resource into
a separate file. Aspose.Words uses the document file name and a unique number to generate unique file name
for each resource found in the document.

[ResourceSavingArgs](./) allows to redefine how resource file names are generated or to
completely circumvent saving of resources into files by providing your own stream objects.

To apply your own logic for generating resource file names use the
[ResourceSavingArgs.resource_file_name](./resource_file_name/) property.

To save resources into streams instead of files, use the [ResourceSavingArgs.resource_stream](./resource_stream/) property.




### Properties

| Name | Description |
| --- | --- |
| [document](./document/) | Gets the document object that is currently being saved. |
| [keep_resource_stream_open](./keep_resource_stream_open/) | Specifies whether Aspose.Words should keep the stream open or close it after saving a resource. |
| [resource_file_name](./resource_file_name/) | Gets or sets the file name (without path) where the resource will be saved to. |
| [resource_file_uri](./resource_file_uri/) | Gets or sets the uniform resource identifier (URI) used to reference the resource file from the document. |
| [resource_stream](./resource_stream/) | Allows to specify the stream where the resource will be saved to. |

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

* module [aspose.words.saving](../)

