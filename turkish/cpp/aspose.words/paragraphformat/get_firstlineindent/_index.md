---
title: "Aspose::Words::ParagraphFormat::get_FirstLineIndent yöntemi"
linktitle: "get_FirstLineIndent"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_FirstLineIndent yöntemi. İlk satır veya sarkan girinti için değeri (puan cinsinden) alır veya ayarlar. İlk satır girintisini ayarlamak için pozitif, sarkan girintiyi ayarlamak için negatif değerler kullanılır C++'ta."
type: docs
weight: 13000
url: /tr/cpp/aspose.words/paragraphformat/get_firstlineindent/
---
## ParagraphFormat::get_FirstLineIndent method


İlk satır veya sarkıt girinti için değeri (puan cinsinden) alır veya ayarlar. İlk satır girintisini ayarlamak için pozitif değerleri, sarkıt girintisini ayarlamak için negatif değerleri kullanın.

```cpp
double Aspose::Words::ParagraphFormat::get_FirstLineIndent()
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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
