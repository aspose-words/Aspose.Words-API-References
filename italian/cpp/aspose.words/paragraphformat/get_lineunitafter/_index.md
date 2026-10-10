---
title: "Aspose::Words::ParagraphFormat::get_LineUnitAfter metodo"
linktitle: "get_LineUnitAfter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ParagraphFormat::get_LineUnitAfter metodo. Ottiene o imposta la quantità di spaziatura (in linee di griglia) dopo i paragrafi in C++."
type: docs
weight: 23000
url: /it/cpp/aspose.words/paragraphformat/get_lineunitafter/
---
## ParagraphFormat::get_LineUnitAfter method


Ottiene o imposta la quantità di spazio (in linee di griglia) dopo i paragrafi.

```cpp
double Aspose::Words::ParagraphFormat::get_LineUnitAfter()
```


## Esempi



Mostra come modificare la spaziatura e i rientri dei paragrafi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();

// Di seguito sono riportate cinque diverse opzioni di spaziatura, insieme alle proprietà che la loro configurazione influisce indirettamente.
// 1 -  Rientro sinistro:
ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 0.0);

format->set_CharacterUnitLeftIndent(10.0);

ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 120.0);

// 2 -  Rientro destro:
ASPOSE_ASSERT_EQ(format->get_RightIndent(), 0.0);

format->set_CharacterUnitRightIndent(-5.5);

ASPOSE_ASSERT_EQ(format->get_RightIndent(), -66.0);

// 3 -  Rientro sporgente:
ASPOSE_ASSERT_EQ(format->get_FirstLineIndent(), 0.0);

format->set_CharacterUnitFirstLineIndent(20.3);

ASSERT_NEAR(format->get_FirstLineIndent(), 243.59, 0.1);

// 4 -  Interlinea prima dei paragrafi:
ASPOSE_ASSERT_EQ(format->get_SpaceBefore(), 0.0);

format->set_LineUnitBefore(5.1);

ASSERT_NEAR(format->get_SpaceBefore(), 61.1, 0.1);

// 5 -  Interlinea dopo i paragrafi:
ASPOSE_ASSERT_EQ(format->get_SpaceAfter(), 0.0);

format->set_LineUnitAfter(10.9);

ASSERT_NEAR(format->get_SpaceAfter(), 130.8, 0.1);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试") + u"文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

## Vedi anche

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
