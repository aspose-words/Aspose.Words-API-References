---
title: ResourceLoadingArgs.uri property
linktitle: uri property
articleTitle: uri property
second_title: Aspose.Words for Python
description: "ResourceLoadingArgs.uri property. URI of the resource which is used for downloading if Aspose.Words.Loading.IResourceLoadingCallback.ResourceLoading(Aspose.Words.Loading.ResourceLoadingArgs) returns [ResourceLoadingAction.DEFAULT](../../resourceloadingaction/#DEFAULT)."
type: docs
weight: 30
url: /python-net/aspose.words.loading/resourceloadingargs/uri/
---

## ResourceLoadingArgs.uri property

URI of the resource which is used for downloading
if Aspose.Words.Loading.IResourceLoadingCallback.ResourceLoading(Aspose.Words.Loading.ResourceLoadingArgs)
returns [ResourceLoadingAction.DEFAULT](../../resourceloadingaction/#DEFAULT).

Initially it's set to absolute URI of the resource,
but user can redefine it to any value.




```python
@property
def uri(self) -> str:
    ...

@uri.setter
def uri(self, value: str):
    ...

```

### See Also

* module [aspose.words.loading](../../)
* class [ResourceLoadingArgs](../)

