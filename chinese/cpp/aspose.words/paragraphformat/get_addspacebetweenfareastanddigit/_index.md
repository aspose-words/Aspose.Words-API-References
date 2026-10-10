---
title: "Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndDigit 方法"
linktitle: "get_AddSpaceBetweenFarEastAndDigit"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndDigit 方法。获取或设置一个标志，指示在 C++ 中当前段落的数字区域与东亚文本区域之间是否自动调整字符间距。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/paragraphformat/get_addspacebetweenfareastanddigit/
---
## ParagraphFormat::get_AddSpaceBetweenFarEastAndDigit method


获取或设置一个标志，指示是否在当前段落的数字区域和东亚文本区域之间自动调整字符间距。

```cpp
bool Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndDigit()
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
