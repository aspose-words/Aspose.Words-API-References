---
title: "Aspose::Words::Paragraph::get_IsEndOfDocument yöntemi"
linktitle: "get_IsEndOfDocument"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Paragraph::get_IsEndOfDocument yöntemi. Bu paragraf, belgenin son bölümündeki son paragraf ise Doğru; C++'da."
type: docs
weight: 9000
url: /tr/cpp/aspose.words/paragraph/get_isendofdocument/
---
## Paragraph::get_IsEndOfDocument method


Bu paragraf belgenin son bölümündeki son paragraf ise doğru.

```cpp
bool Aspose::Words::Paragraph::get_IsEndOfDocument()
```


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

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
