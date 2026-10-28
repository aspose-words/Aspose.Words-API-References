---
title: Aspose::Words::Saving::MarkdownSaveOptions::get_ResourceSavingCallback method
linktitle: get_ResourceSavingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MarkdownSaveOptions::get_ResourceSavingCallback method. Allows to control how resources are saved when a document is exported to Markdown format in C++.'
type: docs
weight: 10208
url: /cpp/aspose.words.saving/markdownsaveoptions/get_resourcesavingcallback/
---
## MarkdownSaveOptions::get_ResourceSavingCallback method


Allows to control how resources are saved when a document is exported to [Markdown](../../../aspose.words/saveformat/) format.

```cpp
const System::SharedPtr<Aspose::Words::Saving::IResourceSavingCallback> & Aspose::Words::Saving::MarkdownSaveOptions::get_ResourceSavingCallback() const
```

## Remarks

 Note, there is only one type of resources in Markdown. These are images. When you specify both [ImageSavingCallback](../get_imagesavingcallback/) and [ResourceSavingCallback](./), then first is called [ResourceSavingCallback](./). However, note it is not necessary to have both implementations, as [ImageSavingArgs](../../imagesavingargs/) is actually a subset of [ResourceSavingArgs](../../resourcesavingargs/). 
## See Also

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
