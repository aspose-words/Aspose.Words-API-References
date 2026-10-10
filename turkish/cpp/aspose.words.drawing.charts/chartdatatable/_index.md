---
title: "Aspose::Words::Drawing::Charts::ChartDataTable class"
linktitle: "ChartDataTable"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartDataTable sınıfı. C++'ta bir grafik veri tablosunun özelliklerini belirtmeye olanak tanır."
type: docs
weight: 9500
url: /tr/cpp/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class


Bir grafik veri tablosunun özelliklerini belirtmeye olanak tanır.

```cpp
class ChartDataTable : public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Font](./get_font/)() | Veri tablosunun yazı tipi biçimlendirmesine erişim sağlar. |
| [get_Format](./get_format/)() | Veri tablosunun metin arka plan doldurmasına ve kenar biçimlendirmesine erişim sağlar. |
| [get_HasHorizontalBorder](./get_hashorizontalborder/)() const | Veri tablosunun yatay kenarının gösterilip gösterilmeyeceğini belirten bir bayrağı alır veya ayarlar. Varsayılan değer **true**'dır. |
| [get_HasLegendKeys](./get_haslegendkeys/)() const | Veri tablosunda efsane anahtarlarının gösterilip gösterilmeyeceğini belirten bir bayrağı alır veya ayarlar. Varsayılan değer **true**'dır. |
| [get_HasOutlineBorder](./get_hasoutlineborder/)() const | Seri ve kategori adlarının etrafındaki bir dış kenarın, yani bir taslak kenarın gösterilip gösterilmeyeceğini belirten bir bayrağı alır veya ayarlar. Varsayılan değer **true**'dır. |
| [get_HasVerticalBorder](./get_hasverticalborder/)() const | Veri tablosunun dikey kenarının gösterilip gösterilmeyeceğini belirten bir bayrağı alır veya ayarlar. Varsayılan değer **true**'dır. |
| [get_Show](./get_show/)() const | Grafik için veri tablosunun gösterilip gösterilmeyeceğini belirten bir bayrağı alır veya ayarlar. Varsayılan değer **false**'dır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_HasHorizontalBorder](./set_hashorizontalborder/)(bool) | [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasHorizontalBorder](./get_hashorizontalborder/) için ayarlayıcı. |
| [set_HasLegendKeys](./set_haslegendkeys/)(bool) | [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasLegendKeys](./get_haslegendkeys/) için ayarlayıcı. |
| [set_HasOutlineBorder](./set_hasoutlineborder/)(bool) | [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasOutlineBorder](./get_hasoutlineborder/) için ayarlayıcı. |
| [set_HasVerticalBorder](./set_hasverticalborder/)(bool) | [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasVerticalBorder](./get_hasverticalborder/) için ayarlayıcı. |
| [set_Show](./set_show/)(bool) | [Aspose::Words::Drawing::Charts::ChartDataTable::get_Show](./get_show/) için ayarlayıcı. |
| static [Type](./type/)() |  |

## Örnekler



Grafik serisi verileriyle veri tablosunun nasıl gösterileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();
auto xValues = System::MakeArray<double>({2020, 2021, 2022, 2023});
series->Add(u"Series1", xValues, System::MakeArray<double>({5, 11, 2, 7}));
series->Add(u"Series2", xValues, System::MakeArray<double>({6, 5.5, 7, 7.8}));
series->Add(u"Series3", xValues, System::MakeArray<double>({10, 8, 7, 9}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataTable> dataTable = chart->get_DataTable();
dataTable->set_Show(true);

dataTable->set_HasLegendKeys(false);
dataTable->set_HasHorizontalBorder(false);
dataTable->set_HasVerticalBorder(false);
dataTable->set_HasOutlineBorder(false);

dataTable->get_Font()->set_Italic(true);
dataTable->get_Format()->get_Stroke()->set_Weight(1);
dataTable->get_Format()->get_Stroke()->set_DashStyle(Aspose::Words::Drawing::DashStyle::ShortDot);
dataTable->get_Format()->get_Stroke()->set_Color(System::Drawing::Color::get_DarkBlue());

doc->Save(get_ArtifactsDir() + u"Charts.DataTable.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
