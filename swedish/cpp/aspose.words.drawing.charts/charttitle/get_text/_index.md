---
title: "Aspose::Words::Drawing::Charts::ChartTitle::get_Text metod"
linktitle: "get_Text"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartTitle::get_Text metod. Hämtar eller anger texten för diagramtiteln. Om null eller ett tomt värde anges, visas en automatiskt genererad titel i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.drawing.charts/charttitle/get_text/
---
## ChartTitle::get_Text method


Hämtar eller anger texten för diagramtiteln. Om **null** eller ett tomt värde anges, visas en automatiskt genererad titel.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartTitle::get_Text()
```


## Exempel



Visar hur man infogar ett diagram och anger en titel.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en diagramform med en dokumentbyggare och hämta dess diagram.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Använd egenskapen "Title" för att ge vårt diagram en titel, som visas i diagramområdets övre centrum.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// Ställ in egenskapen "Show" till "true" för att göra titeln synlig.
title->set_Show(true);

// Ställ in egenskapen "Overlay" till "true" för att ge andra diagramelement mer utrymme genom att låta dem överlappa titeln.
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## Se även

* Class [ChartTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
