---
title: "Aspose::Words::Border class"
linktitle: "Border"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Border class. Bir nesnenin kenarlığını temsil eder. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 7000
url: /tr/cpp/aspose.words/border/
---
## Border class


Bir nesnenin kenarlığını temsil eder. Daha fazla bilgi için, [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) dokümantasyon makalesini ziyaret edin.

```cpp
class Border : public Aspose::Words::InternableComplexAttr,
               public Aspose::Words::IComplexAttr
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Kenarlık özelliklerini varsayılan değerlere sıfırlar. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Border\>\&) | Belirtilen kenarlığın mevcut kenarlıkla değer olarak eşit olup olmadığını belirler. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Belirtilen nesnenin mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| [get_Color](./get_color/)() | Kenar rengini alır veya ayarlar. |
| [get_DistanceFromText](./get_distancefromtext/)() | Kenarlığın metinden veya sayfa kenarından puan cinsinden uzaklığını alır veya ayarlar. |
| [get_IsVisible](./get_isvisible/)() | Eğer [LineStyle](./get_linestyle/) [None](../linestyle/) değilse **true** döndürür. |
| [get_LineStyle](./get_linestyle/)() | Kenar stilini alır veya ayarlar. |
| [get_LineWidth](./get_linewidth/)() | Kenar genişliğini puan cinsinden alır veya ayarlar. |
| [get_Shadow](./get_shadow/)() | Kenarın gölgesi olup olmadığını gösteren bir değeri alır veya ayarlar. |
| [get_ThemeColor](./get_themecolor/)() | Bu [Border](./) nesnesiyle ilişkili uygulanan renk şemasındaki tema rengini alır veya ayarlar. |
| [get_TintAndShade](./get_tintandshade/)() | Bir rengi açan veya karartan çift bir değeri alır veya ayarlar. |
| [GetHashCode](./gethashcode/)() const override | Bu tip için bir karma (hash) işlevi olarak hizmet verir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | [Aspose::Words::Border::get_Color](./get_color/) için ayarlayıcı. |
| [set_DistanceFromText](./set_distancefromtext/)(double) | [Aspose::Words::Border::get_DistanceFromText](./get_distancefromtext/) için ayarlayıcı. |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | [Aspose::Words::Border::get_LineStyle](./get_linestyle/) için ayarlayıcı. |
| [set_LineWidth](./set_linewidth/)(double) | [Aspose::Words::Border::get_LineWidth](./get_linewidth/) için ayarlayıcı. |
| [set_Shadow](./set_shadow/)(bool) | [Aspose::Words::Border::get_Shadow](./get_shadow/) için ayarlayıcı. |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | Ayarlayıcı [Aspose::Words::Border::get_ThemeColor](./get_themecolor/). |
| [set_TintAndShade](./set_tintandshade/)(double) | Ayarlayıcı [Aspose::Words::Border::get_TintAndShade](./get_tintandshade/). |
| static [Type](./type/)() |  |
## Açıklamalar


Kenarlıklar, paragraf, paragraf içindeki metin akışı veya bir tablo hücresi gibi çeşitli belge öğelerine uygulanabilir.

## Örnekler



Bir dizeyi kenarlıkla çevreleyerek belgeye nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


Üst kenarlıklı bir paragrafın nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// ThemeColor yalnızca LineWidth veya LineStyle ayarlandığında ayarlayın.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Ayrıca Bakınız

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
