---
title: "Aspose::Words::Drawing::Charts::ChartLegendEntry sınıfı"
linktitle: "ChartLegendEntry"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartLegendEntry sınıfı. Bir grafik lejand girişi temsil eder. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class


Bir grafik lejand girişini temsil eder. Daha fazla bilgi için, [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) dokümantasyon makalesini ziyaret edin.

```cpp
class ChartLegendEntry : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                         public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Font](./get_font/)() | Bu lejand girişinin yazı tipi biçimlendirmesine erişim sağlar. |
| [get_IsHidden](./get_ishidden/)() const | Bu girişin grafik lejandında gizli olup olmadığını belirten bir değeri alır veya ayarlar. Varsayılan değer **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartLegendEntry::get_IsHidden](./get_ishidden/). |
| static [Type](./type/)() |  |
## Açıklamalar


Bir lejand girişi belirli bir grafik serisi veya trend çizgisine karşılık gelir.

Girişin metni, serinin veya trend çizgisinin adıdır. Metin değiştirilemez.

## Örnekler



Lejand yazı tipiyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> chartLegend = chart->get_Legend();
// Tüm lejand girişleri için varsayılan yazı tipi boyutunu ayarla.
chartLegend->get_Font()->set_Size(14);
// Belirli bir lejand girişi için yazı tipini değiştir.
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Italic(true);
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Size(12);
// Grafik serisi için lejand girişini al.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry> legendEntry = chart->get_Series()->idx_get(0)->get_LegendEntry();

doc->Save(get_ArtifactsDir() + u"Charts.LegendFont.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
