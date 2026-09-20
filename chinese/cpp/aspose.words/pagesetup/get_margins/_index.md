---
title: "Aspose::Words::PageSetup::get_Margins 方法"
linktitle: "get_Margins"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_Margins 方法。返回或设置页面的预设 Margins，使用 C++。"
type: docs
weight: 28000
url: /zh/cpp/aspose.words/pagesetup/get_margins/
---
## PageSetup::get_Margins method


返回或设置页面的预设 [Margins](../../margins/)。

```cpp
Aspose::Words::Margins Aspose::Words::PageSetup::get_Margins()
```


## 示例



显示何时重新计算文档的页面布局。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// 首次将文档保存为 PDF、图像或打印时，将自动
// 缓存文档在各页中的布局。
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// 以某种方式修改文档。
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// 在当前版本的 Aspose.Words 中，修改文档不会自动重建
// 缓存的页面布局。如果我们希望缓存的布局
// 保持最新，需要手动更新。
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## 另见

* Enum [Margins](../../margins/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
