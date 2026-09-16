---
title: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter 方法"
linktitle: "get_OddAndEvenPagesHeaderFooter"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter 方法。如果文档在奇数页和偶数页具有不同的页眉和页脚，则返回 true（在 C++ 中）。"
type: docs
weight: 30000
url: /zh/cpp/aspose.words/pagesetup/get_oddandevenpagesheaderfooter/
---
## PageSetup::get_OddAndEvenPagesHeaderFooter method


如果文档对奇数页和偶数页使用不同的页眉和页脚，则为 true。

```cpp
bool Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter() const
```


## 示例



展示如何启用或禁用偶数页的页眉/页脚。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 以下是两种页眉/页脚类型。
// 1 -  "Primary" 页眉/页脚，出现在章节的每一页上。
// 我们可以通过首页和偶数页的页眉/页脚来覆盖主页眉/页脚。
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

// 2 -  "Even" 页眉/页脚，出现在本章节的每个偶数页上。
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderEven);
builder->Writeln(u"Even page header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterEven);
builder->Writeln(u"Even page footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// 每个章节都有一个 "PageSetup" 对象，用于指定页面外观相关的属性
// 例如方向、尺寸和边框。
// 将 "OddAndEvenPagesHeaderFooter" 属性设置为 "true"
// 在偶数页上显示偶数页页眉/页脚。
// 将 "OddAndEvenPagesHeaderFooter" 属性设置为 "false"
// 在偶数页上显示主页眉/页脚。
builder->get_PageSetup()->set_OddAndEvenPagesHeaderFooter(oddAndEvenPagesHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

## 另见

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
