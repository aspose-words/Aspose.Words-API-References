---
title: "Aspose::Words::Margins 枚举"
linktitle: "Margins"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Margins 枚举。指定 C++ 中的预设页边距。"
type: docs
weight: 99000
url: /zh/cpp/aspose.words/margins/
---
## Margins enum


指定预设的边距。

```cpp
enum class Margins
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 普通 | 0 | 普通页边距。 |
| Narrow | 1 | 窄边距。 |
| 适中 | 2 | 适中边距。 |
| 宽阔 | 3 | 宽阔边距。 |
| 镜像 | 4 | 镜像边距。 |
| 自定义 | 5 | 自定义边距。 |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
