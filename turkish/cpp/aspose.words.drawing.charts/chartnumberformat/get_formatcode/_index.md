---
title: "Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode metodu"
linktitle: "get_FormatCode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode metodu. C++'ta bir veri etiketine uygulanan format kodunu alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.drawing.charts/chartnumberformat/get_formatcode/
---
## ChartNumberFormat::get_FormatCode method


Bir veri etiketine uygulanan format kodunu alır veya ayarlar.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode()
```

## Açıklamalar


Sayı biçimlendirme, bir değerin veri etiketinde nasıl göründüğünü değiştirmek için kullanılır ve bazı çok yaratıcı şekillerde kullanılabilir. Sayı biçimlerinin örnekleri:

Sayı - "#,##0.00"

Para birimi - "\"\$\\"#,##0.00"

Zaman - "[$-x-systime]h:mm:ss AM/PM"

Tarih - "d/mm/yyyy"

Yüzde - "0.00%"

Kesir - "# ?/?"

Bilimsel - "0.00E+00"

Metin - "@"

Muhasebe - "_-\"\$\\"* #,##0.00_-;-\"\$\\"* #,##0.00_-;_-\"\$\\"* \"-\\"??_-;_-@_-"

Renkli özel - "[Red]-#,##0.0"

## Örnekler



Bir grafik serisi için veri etiketlerini nasıl etkinleştirip yapılandıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir çizgi grafik ekleyin, ardından temiz bir grafikle başlamak için demo veri serisini temizleyin,
// ve ardından bir başlık ayarlayın.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Series()->Clear();
chart->get_Title()->set_Text(u"Monthly sales report");

// X ekseni için ayları kategori olarak kullanan özel bir grafik serisi ekleyin,
// ve Y ekseni için ilgili ondalık miktarları belirtin.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Revenue", System::MakeArray<System::String>({u"January", u"February", u"March"}), System::MakeArray<double>({25.611, 21.439, 33.750}));

// Veri etiketlerini etkinleştirin ve ardından veri etiketlerinde gösterilen değerler için özel bir sayı biçimi uygulayın.
// Bu biçim, gösterilen ondalık değerleri ABD Doları milyonları olarak ele alacaktır.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_NumberFormat()->set_FormatCode(u"\"US$\" #,##0.000\"M\"");
dataLabels->get_Font()->set_Size(12);

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelNumberFormat.docx");
```


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

* Class [ChartNumberFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
