---
title: "Aspose::Words::Drawing::Charts::ChartAxisTitle class"
linktitle: "ChartAxisTitle"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartAxisTitle class. Fornisce l'accesso alle proprietà del titolo dell'asse. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 5750
url: /it/cpp/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class


Fornisce l'accesso alle proprietà del titolo dell'asse. Per saperne di più, visita l'articolo di documentazione [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartAxisTitle : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Font](./get_font/)() | Fornisce l'accesso alla formattazione del carattere del titolo dell'asse. |
| [get_Format](./get_format/)() | Fornisce l'accesso alla formattazione di riempimento e linea del titolo dell'asse. |
| [get_Orientation](./get_orientation/)() | Ottiene o imposta l'orientamento del testo del titolo dell'asse. |
| [get_Overlay](./get_overlay/)() | Determina se altri elementi del grafico possono sovrapporsi al titolo. Il valore predefinito è **false**. |
| [get_Rotation](./get_rotation/)() | Ottiene o imposta la rotazione del titolo dell'asse in gradi. |
| [get_Show](./get_show/)() | Determina se il titolo deve essere mostrato per l'asse. Il valore predefinito è **false**. |
| [get_Text](./get_text/)() | Ottiene o imposta il testo del titolo dell'asse. Se viene specificato **null** o un valore vuoto, verrà mostrato un titolo generato automaticamente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Setter per [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Orientation](./get_orientation/). |
| [set_Overlay](./set_overlay/)(bool) | Setter per [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Overlay](./get_overlay/). |
| [set_Rotation](./set_rotation/)(int32_t) | Setter per [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation](./get_rotation/). |
| [set_Show](./set_show/)(bool) | Setter per [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Show](./get_show/). |
| [set_Text](./set_text/)(const System::String\&) | Setter per [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Text](./get_text/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
