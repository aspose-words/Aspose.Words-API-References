---
title: "Aspose::Words::Document::get_PageCount 方法"
linktitle: "get_PageCount"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_PageCount 方法。获取文档的页数，该页数由最近一次在 C++ 中执行的页面布局操作计算得出。"
type: docs
weight: 43000
url: /zh/cpp/aspose.words/document/get_pagecount/
---
## Document::get_PageCount method


获取文档的页数，该页数由最近的页面布局操作计算得出。

```cpp
int32_t Aspose::Words::Document::get_PageCount()
```


## 示例



展示如何统计文档的页数。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// 验证文档的预期页数。
ASSERT_EQ(3, doc->get_PageCount());

// 获取 PageCount 属性会触发文档的页面布局以计算该值。
// 在将文档渲染为固定页保存格式时，此操作无需重新执行，
// 例如 .pdf。因此可以节省一些时间，尤其是处理更复杂的文档时。
doc->Save(get_ArtifactsDir() + u"Document.GetPageCount.pdf");
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
