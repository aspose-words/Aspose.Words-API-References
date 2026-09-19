---
title: "Aspose::Words::Drawing::Charts::ChartTitle classe"
linktitle: "ChartTitle"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartTitle classe. Fornisce l'accesso alle proprietà del titolo del grafico. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 18000
url: /it/cpp/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class


Fornisce l'accesso alle proprietà del titolo del grafico. Per saperne di più, visita l'articolo di documentazione [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartTitle : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Font](./get_font/)() | Fornisce l'accesso alla formattazione del carattere del titolo del grafico. |
| [get_Format](./get_format/)() | Fornisce l'accesso alla formattazione di riempimento e linea del titolo del grafico. |
| [get_Orientation](./get_orientation/)() | Restituisce o imposta l'orientamento del testo del titolo del grafico. |
| [get_Overlay](./get_overlay/)() | Determina se altri elementi del grafico devono poter sovrapporsi al titolo. Per impostazione predefinita, la sovrapposizione è **false**. |
| [get_Rotation](./get_rotation/)() | Restituisce o imposta la rotazione del titolo del grafico in gradi. |
| [get_Show](./get_show/)() | Determina se il titolo deve essere mostrato per questo grafico. Il valore predefinito è **true**. |
| [get_Text](./get_text/)() | Restituisce o imposta il testo del titolo del grafico. Se viene specificato **null** o un valore vuoto, verrà mostrato un titolo generato automaticamente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Setter per [Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation](./get_orientation/). |
| [set_Overlay](./set_overlay/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay](./get_overlay/). |
| [set_Rotation](./set_rotation/)(int32_t) | Impostatore per [Aspose::Words::Drawing::Charts::ChartTitle::get_Rotation](./get_rotation/). |
| [set_Show](./set_show/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartTitle::get_Show](./get_show/). |
| [set_Text](./set_text/)(const System::String\&) | Impostatore per [Aspose::Words::Drawing::Charts::ChartTitle::get_Text](./get_text/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come inserire un grafico e impostare un titolo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci una forma di grafico con un document builder e ottieni il suo grafico.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Usa la proprietà "Title" per dare al nostro grafico un titolo, che appare al centro superiore dell'area del grafico.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// Imposta la proprietà "Show" su "true" per rendere il titolo visibile.
title->set_Show(true);

// Imposta la proprietà "Overlay" su "true" per dare più spazio agli altri elementi del grafico consentendo loro di sovrapporsi al titolo.
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
