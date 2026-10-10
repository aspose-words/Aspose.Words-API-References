---
title: "Aspose::Words::PageSetup::get_CharactersPerLine 方法"
linktitle: "get_CharactersPerLine"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_CharactersPerLine 方法。获取或设置 C++ 中文档网格每行的字符数。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words/pagesetup/get_charactersperline/
---
## PageSetup::get_CharactersPerLine method


获取或设置文档网格中每行的字符数。

```cpp
int32_t Aspose::Words::PageSetup::get_CharactersPerLine()
```

## 备注


属性的最小值为 1。最大值取决于页面宽度和 Normal 样式的字体大小。最小字符间距为字体大小的 90%。例如，Letter 页面在一英寸边距下每行的最大字符数为 43。

默认情况下，属性的值使字符间距等于 Normal 样式的字体大小。

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

## 另见

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
