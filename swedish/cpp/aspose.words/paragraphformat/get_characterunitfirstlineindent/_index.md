---
title: "Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent method"
linktitle: "get_CharacterUnitFirstLineIndent"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent method. Hämtar eller anger värdet (i tecken) för första raden eller hängande indrag. Använd positiva värden för att ange första radens indrag, och negativa värden för att ange hängande indrag i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words/paragraphformat/get_characterunitfirstlineindent/
---
## ParagraphFormat::get_CharacterUnitFirstLineIndent method


Hämtar eller anger värdet (i tecken) för första raden eller hängande indrag. Använd positiva värden för att ange första radens indrag och negativa värden för att ange hängande indrag.

```cpp
double Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent()
```


## Exempel



Visar hur man ändrar styckeavstånd och indrag.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();

// Nedan följer fem olika avståndsalternativ, tillsammans med de egenskaper som deras konfiguration indirekt påverkar.
// 1 -  Vänster indrag:
ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 0.0);

format->set_CharacterUnitLeftIndent(10.0);

ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 120.0);

// 2 -  Höger indrag:
ASPOSE_ASSERT_EQ(format->get_RightIndent(), 0.0);

format->set_CharacterUnitRightIndent(-5.5);

ASPOSE_ASSERT_EQ(format->get_RightIndent(), -66.0);

// 3 -  Hängande indrag:
ASPOSE_ASSERT_EQ(format->get_FirstLineIndent(), 0.0);

format->set_CharacterUnitFirstLineIndent(20.3);

ASSERT_NEAR(format->get_FirstLineIndent(), 243.59, 0.1);

// 4 -  Radavstånd före stycken:
ASPOSE_ASSERT_EQ(format->get_SpaceBefore(), 0.0);

format->set_LineUnitBefore(5.1);

ASSERT_NEAR(format->get_SpaceBefore(), 61.1, 0.1);

// 5 -  Radavstånd efter stycken:
ASPOSE_ASSERT_EQ(format->get_SpaceAfter(), 0.0);

format->set_LineUnitAfter(10.9);

ASSERT_NEAR(format->get_SpaceAfter(), 130.8, 0.1);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试") + u"文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

## Se även

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
