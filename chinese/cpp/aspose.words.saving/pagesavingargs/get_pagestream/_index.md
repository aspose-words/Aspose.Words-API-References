---
title: "Aspose::Words::Saving::PageSavingArgs::get_PageStream 方法"
linktitle: "get_PageStream"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PageSavingArgs::get_PageStream 方法。允许在 C++ 中指定文档页面将保存到的流。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.saving/pagesavingargs/get_pagestream/
---
## PageSavingArgs::get_PageStream method


允许指定文档页面将保存到的流。

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::PageSavingArgs::get_PageStream() const
```

## 备注


此属性允许您将文档页面保存到流中，而不是文件。

默认值为 **null**。当此属性为 **null** 时，文档页面将保存到在 [PageFileName](../get_pagefilename/) 属性中指定的文件。

如果同时设置了 [PageStream](./) 和 [PageFileName](../get_pagefilename/)，则将使用 PageStream。

## 另见

* Class [PageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
