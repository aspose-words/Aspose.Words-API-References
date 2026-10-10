---
title: "Aspose::Words::PageSetup::get_LayoutMode 方法"
linktitle: "get_LayoutMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_LayoutMode 方法。获取或设置此节在 C++ 中的布局模式。"
type: docs
weight: 21000
url: /zh/cpp/aspose.words/pagesetup/get_layoutmode/
---
## PageSetup::get_LayoutMode method


获取或设置本节的布局模式。

```cpp
Aspose::Words::SectionLayoutMode Aspose::Words::PageSetup::get_LayoutMode()
```


## 示例



展示如何指定每行可能拥有的字符数。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 启用间距，然后使用它来设置本节中每行的字符数。
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::Grid);
builder->get_PageSetup()->set_CharactersPerLine(10);

// 字符数还取决于字体大小。
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(20);

ASSERT_EQ(8, doc->get_FirstSection()->get_PageSetup()->get_CharactersPerLine());

builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CharactersPerLine.docx");
```


展示如何为每页可能的行数指定限制。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 启用间距，然后使用它来设置本节中每页的行数。
// 足够大的字体大小会将部分行推到下一页，以避免字符重叠。
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::LineGrid);
builder->get_PageSetup()->set_LinesPerPage(15);

builder->get_ParagraphFormat()->set_SnapToGrid(true);

for (int32_t i = 0; i < 30; i++)
{
    builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
}

doc->Save(get_ArtifactsDir() + u"PageSetup.LinesPerPage.docx");
```

## 另见

* Enum [SectionLayoutMode](../../sectionlayoutmode/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
