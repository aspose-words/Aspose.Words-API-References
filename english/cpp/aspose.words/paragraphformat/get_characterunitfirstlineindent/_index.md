---
title: Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent method
linktitle: get_CharacterUnitFirstLineIndent
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent method. Gets or sets the value (in characters) for the first-line or hanging indent. Use positive values to set the first-line indent, and negative values to set the hanging indent in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words/paragraphformat/get_characterunitfirstlineindent/
---
## ParagraphFormat::get_CharacterUnitFirstLineIndent method


Gets or sets the value (in characters) for the first-line or hanging indent. Use positive values to set the first-line indent, and negative values to set the hanging indent.

```cpp
double Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent()
```


## Examples



Shows how to change paragraph spacing and indents. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();

// Below are five different spacing options, along with the properties that their configuration indirectly affects.
// 1 -  Left indent:
ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 0.0);

format->set_CharacterUnitLeftIndent(10.0);

ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 120.0);

// 2 -  Right indent:
ASPOSE_ASSERT_EQ(format->get_RightIndent(), 0.0);

format->set_CharacterUnitRightIndent(-5.5);

ASPOSE_ASSERT_EQ(format->get_RightIndent(), -66.0);

// 3 -  Hanging indent:
ASPOSE_ASSERT_EQ(format->get_FirstLineIndent(), 0.0);

format->set_CharacterUnitFirstLineIndent(20.3);

ASSERT_NEAR(format->get_FirstLineIndent(), 243.59, 0.1);

// 4 -  Line spacing before paragraphs:
ASPOSE_ASSERT_EQ(format->get_SpaceBefore(), 0.0);

format->set_LineUnitBefore(5.1);

ASSERT_NEAR(format->get_SpaceBefore(), 61.1, 0.1);

// 5 -  Line spacing after paragraphs:
ASPOSE_ASSERT_EQ(format->get_SpaceAfter(), 0.0);

format->set_LineUnitAfter(10.9);

ASSERT_NEAR(format->get_SpaceAfter(), 130.8, 0.1);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试") + u"文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

## See Also

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
