---
title: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream 方法"
linktitle: "get_ResourceStream"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream 方法。允许在 C++ 中指定资源将保存到的流。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.saving/resourcesavingargs/get_resourcestream/
---
## ResourceSavingArgs::get_ResourceStream method


允许指定资源将要保存的流。

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream() const
```

## 备注


此属性允许您将资源保存到流中，而不是文件。

默认值为 **null**。当此属性为 **null** 时，资源将保存到在 [ResourceFileName](../get_resourcefilename/) 属性中指定的文件。

使用 [IResourceSavingCallback](../../iresourcesavingcallback/) 时，您无法将一个资源替换为另一个资源。它仅用于控制资源保存位置。

## 另见

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
