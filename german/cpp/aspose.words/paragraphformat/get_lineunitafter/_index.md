---
title: "Aspose::Words::ParagraphFormat::get_LineUnitAfter-Methode"
linktitle: "get_LineUnitAfter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_LineUnitAfter-Methode. Gibt die Menge des Abstands (in Rasterlinien) nach den Absätzen in C++ zurück oder legt sie fest."
type: docs
weight: 23000
url: /de/cpp/aspose.words/paragraphformat/get_lineunitafter/
---
## ParagraphFormat::get_LineUnitAfter method


Liest oder legt den Abstand (in Rasterlinien) nach den Absätzen fest.

```cpp
double Aspose::Words::ParagraphFormat::get_LineUnitAfter()
```


## Beispiele



Zeigt, wie man Absatzabstände und Einzüge ändert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();

// Unten sind fünf verschiedene Abstandoptionen aufgeführt, zusammen mit den Eigenschaften, die ihre Konfiguration indirekt beeinflussen.
// 1 -  Linker Einzug:
ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 0.0);

format->set_CharacterUnitLeftIndent(10.0);

ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 120.0);

// 2 -  Rechter Einzug:
ASPOSE_ASSERT_EQ(format->get_RightIndent(), 0.0);

format->set_CharacterUnitRightIndent(-5.5);

ASPOSE_ASSERT_EQ(format->get_RightIndent(), -66.0);

// 3 -  Hängender Einzug:
ASPOSE_ASSERT_EQ(format->get_FirstLineIndent(), 0.0);

format->set_CharacterUnitFirstLineIndent(20.3);

ASSERT_NEAR(format->get_FirstLineIndent(), 243.59, 0.1);

// 4 -  Zeilenabstand vor Absätzen:
ASPOSE_ASSERT_EQ(format->get_SpaceBefore(), 0.0);

format->set_LineUnitBefore(5.1);

ASSERT_NEAR(format->get_SpaceBefore(), 61.1, 0.1);

// 5 -  Zeilenabstand nach Absätzen:
ASPOSE_ASSERT_EQ(format->get_SpaceAfter(), 0.0);

format->set_LineUnitAfter(10.9);

ASSERT_NEAR(format->get_SpaceAfter(), 130.8, 0.1);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试") + u"文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

## Siehe auch

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
