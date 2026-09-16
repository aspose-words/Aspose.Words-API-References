---
title: "Aspose::Words::DocumentBuilder::InsertParagraph 方法"
linktitle: "InsertParagraph"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertParagraph 方法。在 C++ 中向文档插入段落换行符。"
type: docs
weight: 44000
url: /zh/cpp/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder::InsertParagraph method


在文档中插入段落换行符。

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::DocumentBuilder::InsertParagraph()
```


### ReturnValue

刚刚插入的段落节点。它与 [CurrentParagraph](../get_currentparagraph/) 是同一个节点。
## 备注


使用由 [ParagraphFormat](../get_paragraphformat/) 属性指定的当前段落格式。

将当前段落拆分为两段。插入段落后，光标位于新段落的开头。

如果无法在当前光标位置插入段落换行符，将抛出异常。

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

* Class [Paragraph](../../paragraph/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
