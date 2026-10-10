---
title: "Aspose::Words::Drawing::Charts::ChartLegend::get_Font yöntemi"
linktitle: "get_Font"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartLegend::get_Font yöntemi. Lejand girişlerinin varsayılan yazı tipi biçimlendirmesine erişim sağlar. Belirli bir lejand girişi için yazı tipi biçimlendirmesini geçersiz kılmak için C++'ta theFont özelliğini kullanın."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.drawing.charts/chartlegend/get_font/
---
## ChartLegend::get_Font method


Lejand girişlerinin varsayılan yazı tipi biçimlendirmesine erişim sağlar. Belirli bir lejand girişi için yazı tipi biçimlendirmesini geçersiz kılmak için [Font](../../chartlegendentry/get_font/) özelliğini kullanın.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::Charts::ChartLegend::get_Font()
```


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

* Class [Font](../../../aspose.words/font/)
* Class [ChartLegend](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
