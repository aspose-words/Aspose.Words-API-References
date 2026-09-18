---
title: "Methode Aspose::Words::Drawing::Charts::AxisDisplayUnit::get_Document"
linktitle: "get_Document"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Methode Aspose::Words::Drawing::Charts::AxisDisplayUnit::get_Document. Gibt das Dokument zurück, das das übergeordnete Diagramm in C++ enthält."
type: docs
weight: 4000
url: /de/cpp/aspose.words.drawing.charts/axisdisplayunit/get_document/
---
## AxisDisplayUnit::get_Document method


Gibt das Dokument zurück, das das übergeordnete Diagramm enthält.

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::Drawing::Charts::AxisDisplayUnit::get_Document()
```


## Beispiele



Zeigt, wie man die Teilstriche und angezeigten Werte einer Diagrammachse manipuliert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());

// Setze die kleinen Teilstriche der Y-Achse so, dass sie vom Diagrammbereich wegzeigen,
// und die großen Teilstriche die Achse kreuzen.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisY();
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);

// Setze die Y-Achse so, dass sie alle 10 Einheiten einen großen Teilstrich und alle 1 Einheit einen kleinen Teilstrich anzeigt.
axis->set_MajorUnit(10);
axis->set_MinorUnit(1);

// Setze die Grenzen der Y-Achse auf -10 und 20.
// Diese Y-Achse zeigt jetzt 4 große Teilstriche und 27 kleine Teilstriche an.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(20.0));

// Für die X-Achse setze die großen Teilstriche alle 10 Einheiten,
// jeden kleinen Teilstrich alle 2,5 Einheiten.
axis = chart->get_AxisX();
axis->set_MajorUnit(10);
axis->set_MinorUnit(2.5);

// Konfiguriere beide Arten von Teilstrichen, sodass sie innerhalb des Diagrammbereichs erscheinen.
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);

// Setze die Grenzen der X-Achse so, dass die X-Achse 5 große Teilstriche und 12 kleine Teilstriche umfasst.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(30.0));
axis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

ASSERT_EQ(1, axis->get_TickLabels()->get_Spacing());
ASPOSE_ASSERT_EQ(doc, axis->get_DisplayUnit()->get_Document());

// Setze die Teilstrichbeschriftungen so, dass sie ihren Wert in Millionen anzeigen.
axis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Millions);

// Wir können einen spezifischeren Wert festlegen, nach dem die Teilstrichbeschriftungen ihre Werte anzeigen.
// Diese Anweisung ist äquivalent zu der obigen.
axis->get_DisplayUnit()->set_CustomUnit(1000000);

doc->Save(get_ArtifactsDir() + u"Charts.AxisDisplayUnit.docx");
```

## Siehe auch

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [AxisDisplayUnit](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
