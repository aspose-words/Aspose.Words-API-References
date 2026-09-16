---
title: "Aspose::Words::Paragraph::get_IsEndOfDocument 方法"
linktitle: "get_IsEndOfDocument"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Paragraph::get_IsEndOfDocument 方法。如果此段落是文档最后一个章节中的最后一个段落，则为 true（C++）。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words/paragraph/get_isendofdocument/
---
## Paragraph::get_IsEndOfDocument method


如果此段落是文档最后一个章节中的最后一个段落，则为 True。

```cpp
bool Aspose::Words::Paragraph::get_IsEndOfDocument()
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

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
