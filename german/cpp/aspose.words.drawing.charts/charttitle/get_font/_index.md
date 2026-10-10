---
title: "Aspose::Words::Drawing::Charts::ChartTitle::get_Font Methode"
linktitle: "get_Font"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartTitle::get_Font Methode. Stellt Zugriff auf die Schriftformatierung des Diagrammtitels in C++ bereit."
type: docs
weight: 1500
url: /de/cpp/aspose.words.drawing.charts/charttitle/get_font/
---
## ChartTitle::get_Font method


Bietet Zugriff auf die Schriftformatierung des Diagrammtitels.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::Charts::ChartTitle::get_Font()
```


## Beispiele



Zeigt, wie man ein Diagramm einfügt und einen Titel festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie mit einem DocumentBuilder ein Diagramm-Shape ein und erhalten Sie dessen Diagramm.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Verwenden Sie die Eigenschaft "Title", um unserem Diagramm einen Titel zu geben, der oben mittig im Diagrammbereich erscheint.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// Setzen Sie die Eigenschaft "Show" auf "true", um den Titel sichtbar zu machen.
title->set_Show(true);

// Setzen Sie die Eigenschaft "Overlay" auf "true", um anderen Diagrammelementen mehr Platz zu geben, indem sie den Titel überlappen dürfen.
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## Siehe auch

* Class [Font](../../../aspose.words/font/)
* Class [ChartTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
