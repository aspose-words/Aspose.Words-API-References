---
title: "Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries 方法"
linktitle: "get_DoNotDisplayPageBoundaries"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries 方法。关闭在 C++ 中文本顶部与页面上边缘之间的空白显示。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.settings/viewoptions/get_donotdisplaypageboundaries/
---
## ViewOptions::get_DoNotDisplayPageBoundaries method


关闭文本顶部与页面上边缘之间空间的显示。

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries() const
```


## 示例



展示如何在视图选项中隐藏垂直空白以及页眉/页脚。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入跨越 3 页的内容。
builder->Writeln(u"Paragraph 1, Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 2, Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 3, Page 3.");

// 插入页眉和页脚。
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"This is the footer.");

// 此文档包含少量内容，但占用了几整页的空间。
// 将 \"DoNotDisplayPageBoundaries\" 标志设置为 \"true\"，以使旧版本的 Microsoft Word 省略页眉，
// 页脚，以及在显示文档时的大量垂直空白。
// 将 \"DoNotDisplayPageBoundaries\" 标志设置为 \"false\"，以使旧版本的 Microsoft Word
// 正常显示我们的文档。
doc->get_ViewOptions()->set_DoNotDisplayPageBoundaries(doNotDisplayPageBoundaries);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayPageBoundaries.doc");
```

## 另见

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
