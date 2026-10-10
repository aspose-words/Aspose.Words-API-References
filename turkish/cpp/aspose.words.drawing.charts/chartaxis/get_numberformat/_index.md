---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_NumberFormat yöntemi"
linktitle: "get_NumberFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_NumberFormat yöntemi. Eksen için sayı biçimlerini tanımlamayı sağlayan bir ChartNumberFormat nesnesi döndürür C++'ta."
type: docs
weight: 20000
url: /tr/cpp/aspose.words.drawing.charts/chartaxis/get_numberformat/
---
## ChartAxis::get_NumberFormat method


Eksen için sayı biçimlerini tanımlamayı sağlayan bir [ChartNumberFormat](../../chartnumberformat/) nesnesi döndürür.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartNumberFormat> Aspose::Words::Drawing::Charts::ChartAxis::get_NumberFormat()
```


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

* Class [ChartNumberFormat](../../chartnumberformat/)
* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
