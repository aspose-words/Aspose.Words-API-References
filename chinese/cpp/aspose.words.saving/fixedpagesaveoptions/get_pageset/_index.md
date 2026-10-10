---
title: "Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet 方法"
linktitle: "get_PageSet"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet 方法。获取或设置要渲染的页面。默认是文档中的所有页面（C++）。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.saving/fixedpagesaveoptions/get_pageset/
---
## FixedPageSaveOptions::get_PageSet method


获取或设置要渲染的页面。默认是文档中的所有页面。

```cpp
System::SharedPtr<Aspose::Words::Saving::PageSet> Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet() const
```


## 示例



展示如何基于精确的页面索引提取页面。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 向文档添加五页。
for (int32_t i = 1; i < 6; i++)
{
    builder->Write(System::String(u"Page ") + i);
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// 创建一个 "XpsSaveOptions" 对象，我们可以将其传递给文档的 "Save" 方法
// 以修改该方法将文档转换为 .XPS 的方式。
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

// 使用 "PageSet" 属性选择文档的一组页面，以保存到输出 XPS。
// 在本例中，我们将通过零基索引选择仅三页：第 1 页、第 2 页和第 4 页。
xpsOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<int32_t>({0, 1, 3})));

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

## 另见

* Class [PageSet](../../pageset/)
* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
