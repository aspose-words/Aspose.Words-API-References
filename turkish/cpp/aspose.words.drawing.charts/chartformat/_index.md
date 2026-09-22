---
title: "Aspose::Words::Drawing::Charts::ChartFormat sınıfı"
linktitle: "ChartFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartFormat sınıfı. Bir grafik öğesinin biçimlendirmesini temsil eder. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class


Bir grafik öğesinin biçimlendirmesini temsil eder. Daha fazla bilgi için, [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) dokümantasyon makalesini ziyaret edin.

```cpp
class ChartFormat : public Aspose::Words::Drawing::Core::IFillable,
                    public Aspose::Words::Drawing::Core::IStrokable
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Fill](./get_fill/)() | Üst grafik öğesi için doldurma biçimlendirmesini alır. |
| [get_IsDefined](./get_isdefined/)() | Herhangi bir biçimin tanımlanıp tanımlanmadığını gösteren bir bayrak alır. |
| [get_ShapeType](./get_shapetype/)() | Üst grafik öğesinin şekil tipini alır veya ayarlar. |
| [get_Stroke](./get_stroke/)() | Üst grafik öğesi için çizgi biçimlendirmesini alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ShapeType](./set_shapetype/)(Aspose::Words::Drawing::Charts::ChartShapeType) | [Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType](./get_shapetype/) için ayarlayıcı. |
| [SetDefaultFill](./setdefaultfill/)() | Grafik öğesinin doldurmasını varsayılan değere sıfırlar. |
| static [Type](./type/)() |  |

## Örnekler



Grafik biçimlendirmesinin nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Varsayılan olarak oluşturulan serileri sil.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2"});
series->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
series->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));

// Grafik arka planını biçimlendir.
chart->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_DarkSlateGray());

// Eksen işaretçi etiketlerini gizle.
chart->get_AxisX()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);
chart->get_AxisY()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);

// Grafik başlığını biçimlendir.
chart->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// Eksen başlığını biçimlendir.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// Lejantı biçimlendir.
chart->get_Legend()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

doc->Save(get_ArtifactsDir() + u"Charts.ChartFormat.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
