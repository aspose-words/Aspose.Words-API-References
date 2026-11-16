---
title: Aspose::Words::ParagraphFormat::get_LineUnitAfter method
linktitle: get_LineUnitAfter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::get_LineUnitAfter method. Gets or sets the amount of spacing (in gridlines) after the paragraphs in C++.'
type: docs
weight: 23000
url: /cpp/aspose.words/paragraphformat/get_lineunitafter/
---
## ParagraphFormat::get_LineUnitAfter method


Gets or sets the amount of spacing (in gridlines) after the paragraphs.

```cpp
double Aspose::Words::ParagraphFormat::get_LineUnitAfter()
```

## Examples


Shows how to change paragraph spacing and indents.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();

// Below are five different spacing options, along with the properties that their configuration indirectly affects.
// 1 -  Left indent:
ASPOSE_ASSERT_EQ(0.0, format->get_LeftIndent());

format->set_CharacterUnitLeftIndent(10.0);

ASPOSE_ASSERT_EQ(120.0, format->get_LeftIndent());

// 2 -  Right indent:
ASPOSE_ASSERT_EQ(0.0, format->get_RightIndent());

format->set_CharacterUnitRightIndent(-5.5);

ASPOSE_ASSERT_EQ(-66.0, format->get_RightIndent());

// 3 -  Hanging indent:
ASPOSE_ASSERT_EQ(0.0, format->get_FirstLineIndent());

format->set_CharacterUnitFirstLineIndent(20.3);

ASSERT_NEAR(243.59, format->get_FirstLineIndent(), 0.1);

// 4 -  Line spacing before paragraphs:
ASPOSE_ASSERT_EQ(0.0, format->get_SpaceBefore());

format->set_LineUnitBefore(5.1);

ASSERT_NEAR(61.1, format->get_SpaceBefore(), 0.1);

// 5 -  Line spacing after paragraphs:
ASPOSE_ASSERT_EQ(0.0, format->get_SpaceAfter());

format->set_LineUnitAfter(10.9);

ASSERT_NEAR(130.8, format->get_SpaceAfter(), 0.1);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试") + u"文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```
## See Also

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
