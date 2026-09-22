---
title: "Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent yöntemi"
linktitle: "get_CharacterUnitLeftIndent"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent yöntemi. Belirtilen paragraflar için sol girinti değerini (karakter cinsinden) alır veya ayarlar C++'ta."
type: docs
weight: 9000
url: /tr/cpp/aspose.words/paragraphformat/get_characterunitleftindent/
---
## ParagraphFormat::get_CharacterUnitLeftIndent method


Belirtilen paragraflar için sol girinti değerini (karakter cinsinden) alır veya ayarlar.

```cpp
double Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent()
```


## Örnekler



Paragraf aralığını ve girintileri nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();

// Aşağıda beş farklı aralık seçeneği ve yapılandırmalarının dolaylı olarak etkilediği özellikler yer alıyor.
// 1 -  Sol girinti:
ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 0.0);

format->set_CharacterUnitLeftIndent(10.0);

ASPOSE_ASSERT_EQ(format->get_LeftIndent(), 120.0);

// 2 -  Sağ girinti:
ASPOSE_ASSERT_EQ(format->get_RightIndent(), 0.0);

format->set_CharacterUnitRightIndent(-5.5);

ASPOSE_ASSERT_EQ(format->get_RightIndent(), -66.0);

// 3 -  Asılı girinti:
ASPOSE_ASSERT_EQ(format->get_FirstLineIndent(), 0.0);

format->set_CharacterUnitFirstLineIndent(20.3);

ASSERT_NEAR(format->get_FirstLineIndent(), 243.59, 0.1);

// 4 -  Paragraflardan önceki satır aralığı:
ASPOSE_ASSERT_EQ(format->get_SpaceBefore(), 0.0);

format->set_LineUnitBefore(5.1);

ASSERT_NEAR(format->get_SpaceBefore(), 61.1, 0.1);

// 5 -  Paragraflardan sonraki satır aralığı:
ASPOSE_ASSERT_EQ(format->get_SpaceAfter(), 0.0);

format->set_LineUnitAfter(10.9);

ASSERT_NEAR(format->get_SpaceAfter(), 130.8, 0.1);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试") + u"文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

## Ayrıca Bakınız

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
