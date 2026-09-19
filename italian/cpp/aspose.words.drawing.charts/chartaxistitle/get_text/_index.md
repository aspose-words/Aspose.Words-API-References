---
title: "Metodo Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Text"
linktitle: "get_Text"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Text. Ottiene o imposta il testo del titolo dell'asse. Se viene specificato un valore nullo o vuoto, verrà mostrato un titolo generato automaticamente in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.drawing.charts/chartaxistitle/get_text/
---
## ChartAxisTitle::get_Text method


Ottiene o imposta il testo del titolo dell'asse. Se viene specificato **null** o un valore vuoto, verrà mostrato un titolo generato automaticamente.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Text()
```


## Esempi



Mostra come impostare il titolo dell'asse del grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Elimina la serie generata di default.
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

## Vedi anche

* Class [ChartAxisTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
