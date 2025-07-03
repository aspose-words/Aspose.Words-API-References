---
title: Aspose::Words::Drawing::Charts::ChartAxisTitle class
linktitle: ChartAxisTitle
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartAxisTitle class. Provides access to the axis title properties. To learn more, visit the  documentation article in C++.'
type: docs
weight: 5750
url: /cpp/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class


Provides access to the axis title properties. To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article.

```cpp
class ChartAxisTitle : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Font](./get_font/)() | Provides access to the font formatting of the axis title. |
| [get_Format](./get_format/)() | Provides access to fill and line formatting of the axis title. |
| [get_Overlay](./get_overlay/)() | Determines whether other chart elements shall be allowed to overlap the title. The default value is **false**. |
| [get_Show](./get_show/)() | Determines whether the title shall be shown for the axis. The default value is **false**. |
| [get_Text](./get_text/)() | Gets or sets the text of the axis title. If **null** or empty value is specified, auto generated title will be shown. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Overlay](./set_overlay/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Overlay](./get_overlay/). |
| [set_Show](./set_show/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Show](./get_show/). |
| [set_Text](./set_text/)(const System::String\&) | Setter for [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Text](./get_text/). |
| static [Type](./type/)() |  |

## Examples



Shows how to set chart axis title. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Delete default generated series.
seriesColl->Clear();

seriesColl->Add(u"AW Series 1", System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2"}), System::MakeArray<double>({1, 2}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisXTitle = chart->get_AxisX()->get_Title();
chartAxisXTitle->set_Text(u"Categories");
chartAxisXTitle->set_Show(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisYTitle = chart->get_AxisY()->get_Title();
chartAxisYTitle->set_Text(u"Values");
chartAxisYTitle->set_Show(true);
chartAxisYTitle->set_Overlay(true);
chartAxisYTitle->get_Font()->set_Size(12);
chartAxisYTitle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.ChartAxisTitle.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
