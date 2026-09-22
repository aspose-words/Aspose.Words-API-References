---
title: "Aspose::Words::Drawing::Charts::ChartTitle class"
linktitle: "ChartTitle"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartTitle sınıfı. Grafik başlığı özelliklerine erişim sağlar. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 18000
url: /tr/cpp/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class


Grafik başlığı özelliklerine erişim sağlar. Daha fazla bilgi için, [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) dokümantasyon makalesini ziyaret edin.

```cpp
class ChartTitle : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Font](./get_font/)() | Grafik başlığının yazı tipi biçimlendirmesine erişim sağlar. |
| [get_Format](./get_format/)() | Grafik başlığının dolgu ve çizgi biçimlendirmesine erişim sağlar. |
| [get_Orientation](./get_orientation/)() | Grafik başlığı metninin yönünü alır veya ayarlar. |
| [get_Overlay](./get_overlay/)() | Diğer grafik öğelerinin başlığın üzerine gelmesine izin verilip verilmeyeceğini belirler. Varsayılan olarak bindirme **false**'dur. |
| [get_Rotation](./get_rotation/)() | Grafik başlığının derece cinsinden döndürülmesini alır veya ayarlar. |
| [get_Show](./get_show/)() | Bu grafik için başlığın gösterilip gösterilmeyeceğini belirler. Varsayılan değer **true**'dur. |
| [get_Text](./get_text/)() | Grafik başlığının metnini alır veya ayarlar. **null** veya boş bir değer belirtilirse, otomatik oluşturulan başlık gösterilir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | [Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation](./get_orientation/) için ayarlayıcı. |
| [set_Overlay](./set_overlay/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay](./get_overlay/). |
| [set_Rotation](./set_rotation/)(int32_t) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartTitle::get_Rotation](./get_rotation/). |
| [set_Show](./set_show/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartTitle::get_Show](./get_show/). |
| [set_Text](./set_text/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartTitle::get_Text](./get_text/). |
| static [Type](./type/)() |  |

## Örnekler



Bir çizelge eklemeyi ve başlık ayarlamayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir belge oluşturucu ile bir çizelge şekli ekleyin ve onun çizelgesini alın.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// "Title" özelliğini kullanarak çizelgemize bir başlık verin; bu başlık, çizelge alanının üst orta kısmında görünür.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// "Show" özelliğini "true" olarak ayarlayın, böylece başlık görünür olur.
title->set_Show(true);

// "Overlay" özelliğini "true" olarak ayarlayın Başlığa üst üste gelmelerine izin vererek diğer çizelge öğelerine daha fazla alan tanıyın.
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
