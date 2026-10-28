---
title: Aspose::Words::Saving::MarkdownSaveOptions::set_ResourceSavingCallback method
linktitle: set_ResourceSavingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MarkdownSaveOptions::set_ResourceSavingCallback method. Allows to control how resources are saved when a document is exported to Markdown format in C++.'
type: docs
weight: 14750
url: /cpp/aspose.words.saving/markdownsaveoptions/set_resourcesavingcallback/
---
## MarkdownSaveOptions::set_ResourceSavingCallback method


Allows to control how resources are saved when a document is exported to [Markdown](../../../aspose.words/saveformat/) format.

```cpp
void Aspose::Words::Saving::MarkdownSaveOptions::set_ResourceSavingCallback(const System::SharedPtr<Aspose::Words::Saving::IResourceSavingCallback> & value)
```

## Remarks

 Note, there is only one type of resources in Markdown. These are images. When you specify both [ImageSavingCallback](../get_imagesavingcallback/) and [ResourceSavingCallback](../get_resourcesavingcallback/), then first is called [ResourceSavingCallback](../get_resourcesavingcallback/). However, note it is not necessary to have both implementations, as [ImageSavingArgs](../../imagesavingargs/) is actually a subset of [ResourceSavingArgs](../../resourcesavingargs/). 
## See Also

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
