---
title: "Aspose::Words::Drawing::Charts::Chart sınıfı"
linktitle: "Grafik"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::Chart sınıfı. Grafik şekil özelliklerine erişim sağlar. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.drawing.charts/chart/
---
## Chart class


Grafik şekil özelliklerine erişim sağlar. Daha fazla bilgi için, [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) dokümantasyon makalesini ziyaret edin.

```cpp
class Chart : public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Axes](./get_axes/)() | Bu grafiğin tüm eksenlerinin bir koleksiyonunu alır. |
| [get_AxisX](./get_axisx/)() | Grafiğin birincil X ekseninin özelliklerine erişim sağlar. |
| [get_AxisY](./get_axisy/)() | Grafiğin birincil Y ekseninin özelliklerine erişim sağlar. |
| [get_AxisZ](./get_axisz/)() | Grafiğin Z ekseninin özelliklerine erişim sağlar. |
| [get_DataTable](./get_datatable/)() | Bu çizelgenin veri tablosunun özelliklerine erişim sağlar. Veri tablosu, [Show](../chartdatatable/get_show/) özelliği kullanılarak gösterilebilir. |
| [get_Format](./get_format/)() | Çizelgenin dolgu ve çizgi biçimlendirmesine erişim sağlar. |
| [get_Legend](./get_legend/)() | Çizelge açıklama özelliklerine erişim sağlar. |
| [get_Series](./get_series/)() | Seri koleksiyonuna erişim sağlar. |
| [get_SeriesGroups](./get_seriesgroups/)() | Bu çizelgenin seri grup koleksiyonuna erişim sağlar. |
| [get_SourceFullName](./get_sourcefullname/)() | Bu çizelgenin bağlı olduğu xls/xlsx dosyasının yolunu ve adını alır. |
| [get_Style](./get_style/)() | Çizelgenin stilini alır. |
| [get_Title](./get_title/)() | Çizelge başlığı özelliklerine erişim sağlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | [Aspose::Words::Drawing::Charts::Chart::get_SourceFullName](./get_sourcefullname/) için ayarlayıcı. |
| [set_Style](./set_style/)(Aspose::Words::Drawing::Charts::ChartStyle) | Çizelgenin stilini ayarlar. |
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
