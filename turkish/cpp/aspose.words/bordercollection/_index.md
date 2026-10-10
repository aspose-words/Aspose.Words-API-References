---
title: "Aspose::Words::BorderCollection sınıfı"
linktitle: "BorderCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BorderCollection sınıfı. Border nesnelerinin bir koleksiyonu. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 8000
url: /tr/cpp/aspose.words/bordercollection/
---
## BorderCollection class


Bir [Border](../border/) nesneleri koleksiyonu. Daha fazla bilgi edinmek için [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) belge makalesini ziyaret edin.

```cpp
class BorderCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Border>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Bir nesnenin tüm kenarlarını kaldırır. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::BorderCollection\>\&) | Kenar koleksiyonlarını karşılaştırır. |
| [get_Bottom](./get_bottom/)() | Alt kenarı alır. |
| [get_Color](./get_color/)() | Kenar rengini alır veya ayarlar. |
| [get_Count](./get_count/)() | Koleksiyondaki kenar sayısını alır. |
| [get_DistanceFromText](./get_distancefromtext/)() | Kenarın metinden puan cinsinden uzaklığını alır veya ayarlar. |
| [get_Horizontal](./get_horizontal/)() | Hücreler veya uyumlu paragraflar arasında kullanılan yatay kenarı alır. |
| [get_Left](./get_left/)() | Sol kenarı alır. |
| [get_LineStyle](./get_linestyle/)() | Kenar stilini alır veya ayarlar. |
| [get_LineWidth](./get_linewidth/)() | Kenar genişliğini puan cinsinden alır veya ayarlar. |
| [get_Right](./get_right/)() | Sağ kenarı alır. |
| [get_Shadow](./get_shadow/)() | Kenarın gölgesi olup olmadığını gösteren bir değeri alır veya ayarlar. |
| [get_Top](./get_top/)() | Üst kenarı alır. |
| [get_Vertical](./get_vertical/)() | Hücreler arasında kullanılan dikey kenarı alır. |
| [GetEnumerator](./getenumerator/)() override | Koleksiyondaki tüm kenarları yinelemek için kullanılabilecek bir enumerator nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::BorderType) | Kenar tipine göre bir [Border](../border/) nesnesi alır. |
| [idx_get](./idx_get/)(int32_t) | İndexe göre bir [Border](../border/) nesnesi alır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | [Aspose::Words::BorderCollection::get_Color](./get_color/) için ayarlayıcı. |
| [set_DistanceFromText](./set_distancefromtext/)(double) | [Aspose::Words::BorderCollection::get_DistanceFromText](./get_distancefromtext/) için ayarlayıcı. |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | [Aspose::Words::BorderCollection::get_LineStyle](./get_linestyle/) için ayarlayıcı. |
| [set_LineWidth](./set_linewidth/)(double) | [Aspose::Words::BorderCollection::get_LineWidth](./get_linewidth/) için ayarlayıcı |
| [set_Shadow](./set_shadow/)(bool) | Ayarlayıcı for [Aspose::Words::BorderCollection::get_Shadow](./get_shadow/). |
| static [Type](./type/)() |  |

## Örnekler



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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
