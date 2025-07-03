---
title: Aspose::Words::Loading::ResourceLoadingAction enum
linktitle: ResourceLoadingAction
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::ResourceLoadingAction enum. Specifies the mode of resource loading. To learn more, visit the  documentation article in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words.loading/resourceloadingaction/
---
## ResourceLoadingAction enum


Specifies the mode of resource loading. To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) documentation article.

```cpp
enum class ResourceLoadingAction
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Default | 0 | Aspose.Words will load this resource as usual. |
| Skip | 1 | Aspose.Words will skip loading of this resource. Only link without data will be stored for an image, CSS style sheet will be ignored for HTML format. |
| UserProvided | 2 | Aspose.Words will use byte array provided by user in [SetData()](../) as resource data. |

## See Also

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
