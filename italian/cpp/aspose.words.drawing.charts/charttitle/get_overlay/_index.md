---
title: "Metodo Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay"
linktitle: "get_Overlay"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay. Determina se altri elementi del grafico possono sovrapporsi al titolo. Per impostazione predefinita, overlay è false in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.drawing.charts/charttitle/get_overlay/
---
## ChartTitle::get_Overlay method


Determina se altri elementi del grafico devono poter sovrapporsi al titolo. Per impostazione predefinita, la sovrapposizione è **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay()
```


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

* Class [ChartTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
