---
title: "Aspose::Words::SectionLayoutMode 枚举"
linktitle: "SectionLayoutMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::SectionLayoutMode 枚举。指定节的布局模式，允许在 C++ 中定义文档网格行为。"
type: docs
weight: 115000
url: /zh/cpp/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enum


指定节的布局模式，以便定义文档网格行为。

```cpp
enum class SectionLayoutMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Default | 0 | 指定不应对文档中相应节的内容应用文档网格。 |
| 网格 | 1 | 指定相应的节应在其中的每一行和每个字符上同时添加额外的行间距和字符间距，以保持每页特定的行数和每行特定的字符数。字符在输入时不会自动与网格线对齐。 |
| LineGrid | 2 | 指定相应的节应在其中的每一行添加额外的行间距，以保持指定的每页行数。 |
| SnapToChars | 3 | 指定相应的节应在其中的每一行和每个字符上同时添加额外的行间距和字符间距，以保持每页特定的行数和每行特定的字符数。字符在输入时会自动与网格线对齐。 |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
