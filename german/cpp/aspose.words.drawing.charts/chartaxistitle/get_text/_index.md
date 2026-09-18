---
title: "Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Text Methode"
linktitle: "get_Text"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Text Methode. Gibt den Text des Achsentitels zurück oder setzt ihn. Wenn ein null- oder leerer Wert angegeben wird, wird ein automatisch generierter Titel in C++ angezeigt."
type: docs
weight: 6000
url: /de/cpp/aspose.words.drawing.charts/chartaxistitle/get_text/
---
## ChartAxisTitle::get_Text method


Liest oder setzt den Text des Achsentitels. Wenn **null** oder ein leerer Wert angegeben wird, wird ein automatisch generierter Titel angezeigt.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Text()
```


## Beispiele



Zeigt, wie man den Achsentitel eines Diagramms festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Lösche standardmäßig generierte Serie.
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

## Siehe auch

* Class [ChartAxisTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
