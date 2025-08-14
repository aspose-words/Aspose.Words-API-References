---
title: XamlFixedSaveOptions.resources_folder_alias property
linktitle: resources_folder_alias property
articleTitle: resources_folder_alias property
second_title: Aspose.Words for Python
description: "XamlFixedSaveOptions.resources_folder_alias property. Specifies the name of the folder used to construct image URIs written into an fixed page Xaml document"
type: docs
weight: 40
url: /python-net/aspose.words.saving/xamlfixedsaveoptions/resources_folder_alias/
---

## XamlFixedSaveOptions.resources_folder_alias property

Specifies the name of the folder used to construct image URIs written into an fixed page Xaml document.
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

When you save a [Document](../../../aspose.words/document/) in fixed page Xaml format, Aspose.Words needs to save all
images embedded in the document as standalone files. [XamlFixedSaveOptions.resources_folder](../resources_folder/)
allows you to specify where the images will be saved and [XamlFixedSaveOptions.resources_folder_alias](./)
allows to specify how the image URIs will be constructed.




### See Also

* module [aspose.words.saving](../../)
* class [XamlFixedSaveOptions](../)
* property [XamlFixedSaveOptions.resources_folder](../resources_folder/)

