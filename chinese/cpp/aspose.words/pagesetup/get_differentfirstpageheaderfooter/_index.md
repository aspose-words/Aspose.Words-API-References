---
title: "Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter 方法"
linktitle: "get_DifferentFirstPageHeaderFooter"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter 方法。如果在 C++ 中第一页使用了不同的页眉或页脚，则返回 true。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words/pagesetup/get_differentfirstpageheaderfooter/
---
## PageSetup::get_DifferentFirstPageHeaderFooter method


如果首页使用不同的页眉或页脚，则为 true。

```cpp
bool Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter()
```


## 示例



展示如何启用或禁用主要页眉/页脚。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 以下是两种页眉/页脚类型。
// 1 -  \"First\" 页眉/页脚，出现在节的第一页。
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderFirst);
builder->Writeln(u"First page header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterFirst);
builder->Writeln(u"First page footer.");

// 2 -  \"Primary\" 页眉/页脚，出现在节的每一页。
// 我们可以通过首页和偶数页的页眉/页脚来覆盖主页眉/页脚。
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// 每个章节都有一个 "PageSetup" 对象，用于指定页面外观相关的属性
// 例如方向、尺寸和边框。
// 将 \"DifferentFirstPageHeaderFooter\" 属性设置为 \"true\"，以在首页应用第一页的页眉/页脚。
// 将 \"DifferentFirstPageHeaderFooter\" 属性设置为 \"false\"
// 以使首页显示主要页眉/页脚。
builder->get_PageSetup()->set_DifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.DifferentFirstPageHeaderFooter.docx");
```

## 另见

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
