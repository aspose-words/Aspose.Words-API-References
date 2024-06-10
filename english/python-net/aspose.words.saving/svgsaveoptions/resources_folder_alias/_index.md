---
title: SvgSaveOptions.resources_folder_alias property
linktitle: resources_folder_alias property
articleTitle: resources_folder_alias property
second_title: Aspose.Words for Python
description: "SvgSaveOptions.resources_folder_alias property. Specifies the name of the folder used to construct image URIs written into an SVG document"
type: docs
weight: 70
url: /python-net/aspose.words.saving/svgsaveoptions/resources_folder_alias/
---

## SvgSaveOptions.resources_folder_alias property

Specifies the name of the folder used to construct image URIs written into an SVG document.
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

When you save a [Document](../../../aspose.words/document/) in SVG format, Aspose.Words needs to save all
images embedded in the document as standalone files. [SvgSaveOptions.resources_folder](../resources_folder/)
allows you to specify where the images will be saved and [SvgSaveOptions.resources_folder_alias](./)
allows to specify how the image URIs will be constructed.




### See Also

* module [aspose.words.saving](../../)
* class [SvgSaveOptions](../)
* property [SvgSaveOptions.resources_folder](../resources_folder/)

