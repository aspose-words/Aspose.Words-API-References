---
title: "Aspose::Words::FrameFormat sınıfı"
linktitle: "FrameFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::FrameFormat sınıfı. C++'da bir paragraf için çerçeve ile ilgili biçimlendirmeyi temsil eder."
type: docs
weight: 30000
url: /tr/cpp/aspose.words/frameformat/
---
## FrameFormat class


Bir paragraf için çerçeveyle ilgili biçimlendirmeyi temsil eder.

```cpp
class FrameFormat : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Height](./get_height/)() | Belirtilen çerçevenin yüksekliğini alır. |
| [get_HeightRule](./get_heightrule/)() | Belirtilen çerçevenin yüksekliğini belirleme kuralını alır. |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | Belirtilen çerçevenin yatay hizalamasını alır. |
| [get_HorizontalDistanceFromText](./get_horizontaldistancefromtext/)() | Bir çerçeve ile çevresindeki metin arasındaki yatay mesafeyi, puan cinsinden alır. |
| [get_HorizontalPosition](./get_horizontalposition/)() | Çerçevenin kenarı ile [RelativeHorizontalPosition](./get_relativehorizontalposition/) özelliğiyle belirtilen öğe arasındaki yatay mesafeyi alır. |
| [get_IsFrame](./get_isframe/)() | Paragraf bir çerçeve ise **true** döndürür. |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | Bir çerçevenin göreli yatay konumunu alır. |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | Bir çerçevenin göreli dikey konumunu alır. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Belirtilen çerçevenin dikey hizalamasını alır. |
| [get_VerticalDistanceFromText](./get_verticaldistancefromtext/)() | Bir çerçeve ile çevresindeki metin arasındaki dikey mesafeyi (puan cinsinden) belirtir. |
| [get_VerticalPosition](./get_verticalposition/)() | Çerçevenin kenarı ile [RelativeVerticalPosition](./get_relativeverticalposition/) özelliğiyle belirtilen öğe arasındaki dikey mesafeyi alır. |
| [get_Width](./get_width/)() | Belirtilen çerçevenin genişliğini, puan cinsinden alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Açıklamalar


Bu nesne her zaman oluşturulur. Bir paragraf çerçeve ise, tüm özellikler ilgili değerleri içerir, aksi takdirde tüm özellikler varsayılanlarına ayarlanır.

Paragrafın çerçeve olup olmadığını kontrol etmek için [IsFrame](./get_isframe/) kullanın.

## Örnekler



Çerçeve olan paragrafların biçimlendirme özellikleri hakkında bilgi almanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraph frame.docx");

System::SharedPtr<Aspose::Words::Paragraph> paragraphFrame = doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_First(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_FrameFormat()->get_IsFrame();
})));

ASPOSE_ASSERT_EQ(233.3, paragraphFrame->get_FrameFormat()->get_Width());
ASPOSE_ASSERT_EQ(138.8, paragraphFrame->get_FrameFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::AtLeast, paragraphFrame->get_FrameFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::Drawing::HorizontalAlignment::Default, paragraphFrame->get_FrameFormat()->get_HorizontalAlignment());
ASSERT_EQ(Aspose::Words::Drawing::VerticalAlignment::Default, paragraphFrame->get_FrameFormat()->get_VerticalAlignment());
ASPOSE_ASSERT_EQ(34.05, paragraphFrame->get_FrameFormat()->get_HorizontalPosition());
ASSERT_EQ(Aspose::Words::Drawing::RelativeHorizontalPosition::Page, paragraphFrame->get_FrameFormat()->get_RelativeHorizontalPosition());
ASPOSE_ASSERT_EQ(9.0, paragraphFrame->get_FrameFormat()->get_HorizontalDistanceFromText());
ASPOSE_ASSERT_EQ(20.5, paragraphFrame->get_FrameFormat()->get_VerticalPosition());
ASSERT_EQ(Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph, paragraphFrame->get_FrameFormat()->get_RelativeVerticalPosition());
ASPOSE_ASSERT_EQ(0.0, paragraphFrame->get_FrameFormat()->get_VerticalDistanceFromText());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
