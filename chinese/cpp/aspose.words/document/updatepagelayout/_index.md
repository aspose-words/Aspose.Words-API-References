---
title: "Aspose::Words::Document::UpdatePageLayout 方法"
linktitle: "UpdatePageLayout"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::UpdatePageLayout 方法。重新构建文档在 C++ 中的页面布局。"
type: docs
weight: 98000
url: /zh/cpp/aspose.words/document/updatepagelayout/
---
## Document::UpdatePageLayout method


重新构建文档的页面布局。

```cpp
void Aspose::Words::Document::UpdatePageLayout()
```

## 备注


此方法将文档格式化为页面，并更新文档中与页码相关的字段，如 PAGE、PAGES、PAGEREF 和 REF。最新的页面布局信息是将文档正确渲染为固定页格式的必要条件。

首次将文档转换为 PDF、XPS、图像或打印时，会自动调用此方法。然而，如果在渲染后修改文档并再次尝试渲染——Aspose.Words 将不会自动更新页面布局。在这种情况下，您应在再次渲染前调用 [UpdatePageLayout](./)。

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
