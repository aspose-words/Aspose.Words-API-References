---
title: "Aspose::Words::Drawing::Charts::ChartNumberFormat class"
linktitle: "ChartNumberFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartNumberFormat class. Üst öğenin sayı biçimlendirmesini temsil eder. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 15000
url: /tr/cpp/aspose.words.drawing.charts/chartnumberformat/
---
## ChartNumberFormat class


Üst öğenin sayı biçimlendirmesini temsil eder. Daha fazla bilgi için, [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) dokümantasyon makalesini ziyaret edin.

```cpp
class ChartNumberFormat : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_FormatCode](./get_formatcode/)() | Bir veri etiketine uygulanan format kodunu alır veya ayarlar. |
| [get_IsLinkedToSource](./get_islinkedtosource/)() | Format kodunun bir kaynak hücreye bağlı olup olmadığını belirtir. Varsayılan değer true'tir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode](./get_formatcode/). |
| [set_IsLinkedToSource](./set_islinkedtosource/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource](./get_islinkedtosource/). |
| static [Type](./type/)() |  |

## Örnekler



Grafik değerleri için biçimlendirme ayarlamayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart->get_Series()->Clear();

// X ekseni için kategorilerle birlikte grafiğe özel bir seri ekleyin,
// ve Y ekseni için büyük ilgili sayısal değerler.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({1900000, 850000, 2100000, 600000, 1500000}));

// Y ekseni tik etiketlerinin sayı biçimini, rakamları virgülle gruplamayacak şekilde ayarlayın.
chart->get_AxisY()->get_NumberFormat()->set_FormatCode(u"#,##0");

// Bu bayrak, yukarıdaki değeri geçersiz kılabilir ve sayı biçimini kaynak hücreden alabilir.
ASSERT_FALSE(chart->get_AxisY()->get_NumberFormat()->get_IsLinkedToSource());

doc->Save(get_ArtifactsDir() + u"Charts.SetNumberFormatToChartAxis.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
