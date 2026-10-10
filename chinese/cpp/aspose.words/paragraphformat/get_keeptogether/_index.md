---
title: "Aspose::Words::ParagraphFormat::get_KeepTogether 方法"
linktitle: "get_KeepTogether"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_KeepTogether 方法。如果段落中的所有行必须保持在同一页上，则返回 true（在 C++ 中）。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words/paragraphformat/get_keeptogether/
---
## ParagraphFormat::get_KeepTogether method


如果段落中的所有行必须保持在同一页上，则为 True。

```cpp
bool Aspose::Words::ParagraphFormat::get_KeepTogether()
```


## 示例



展示如何向文档插入段落。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Arial");
font->set_Underline(Aspose::Words::Underline::Dash);

System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_FirstLineIndent(8);
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Justify);
paragraphFormat->set_AddSpaceBetweenFarEastAndAlpha(true);
paragraphFormat->set_AddSpaceBetweenFarEastAndDigit(true);
paragraphFormat->set_KeepTogether(true);

// 该 "Writeln" 方法在追加文本后结束段落
// 然后开始新行，添加新段落。
builder->Writeln(u"Hello world!");

ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsEndOfDocument());
```

## 另见

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
