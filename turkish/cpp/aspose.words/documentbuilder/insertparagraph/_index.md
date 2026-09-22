---
title: "Aspose::Words::DocumentBuilder::InsertParagraph yöntemi"
linktitle: "InsertParagraph"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertParagraph yöntemi. C++'ta belgeye bir paragraf sonu ekler."
type: docs
weight: 44000
url: /tr/cpp/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder::InsertParagraph method


Belgeye bir paragraf sonu ekler.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::DocumentBuilder::InsertParagraph()
```


### ReturnValue

Az önce eklenen paragraf düğümü. Bu, [CurrentParagraph](../get_currentparagraph/) ile aynı düğümdür.
## Açıklamalar


Mevcut paragraf biçimlendirmesi, [ParagraphFormat](../get_paragraphformat/) özelliği tarafından belirtilen şekilde kullanılır.

Mevcut paragrafı ikiye böler. Paragraf eklendikten sonra, imleç yeni paragrafın başına yerleştirilir.

Mevcut imleç konumunda bir paragraf sonu eklenemiyorsa bir istisna fırlatılır.

## Örnekler



Bir paragrafın belgeye nasıl ekleneceğini gösterir.
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

// \"Writeln\" yöntemi, metni ekledikten sonra paragrafı sonlandırır
// ve ardından yeni bir satır başlatır, yeni bir paragraf ekler.
builder->Writeln(u"Hello world!");

ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsEndOfDocument());
```

## Ayrıca Bakınız

* Class [Paragraph](../../paragraph/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
