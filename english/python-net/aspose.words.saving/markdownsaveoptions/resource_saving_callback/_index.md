---
title: MarkdownSaveOptions.resource_saving_callback property
linktitle: resource_saving_callback property
articleTitle: resource_saving_callback property
second_title: Aspose.Words for Python
description: "MarkdownSaveOptions.resource_saving_callback property. Allows to control how resources are saved when a document is exported to [SaveFormat.MARKDOWN](../../../aspose.words/saveformat/#MARKDOWN) format."
type: docs
weight: 130
url: /python-net/aspose.words.saving/markdownsaveoptions/resource_saving_callback/
---

## MarkdownSaveOptions.resource_saving_callback property

Allows to control how resources are saved when a document is exported to
[SaveFormat.MARKDOWN](../../../aspose.words/saveformat/#MARKDOWN) format.



```python
@property
def resource_saving_callback(self) -> aspose.words.saving.IResourceSavingCallback:
    ...

@resource_saving_callback.setter
def resource_saving_callback(self, value: aspose.words.saving.IResourceSavingCallback):
    ...

```

### Remarks

Note, there is only one type of resources in Markdown. These are images.
When you specify both [MarkdownSaveOptions.image_saving_callback](../image_saving_callback/) and [MarkdownSaveOptions.resource_saving_callback](./),
then first is called [MarkdownSaveOptions.resource_saving_callback](./). However, note it is not necessary to have both
implementations, as [ImageSavingArgs](../../imagesavingargs/) is actually a subset of [ResourceSavingArgs](../../resourcesavingargs/).



### See Also

* module [aspose.words.saving](../../)
* class [MarkdownSaveOptions](../)

