---
title: "Aspose::Words::Drawing::Charts::AxisBound::get_ValueAsDate‑metod"
linktitle: "get_ValueAsDate"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::AxisBound::get_ValueAsDate‑metod. Returnerar värdet på axelgränsen representerat som datumtid i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.drawing.charts/axisbound/get_valueasdate/
---
## AxisBound::get_ValueAsDate method


Returnerar värdet för axelgränsen representerat som datum/tid.

```cpp
System::DateTime Aspose::Words::Drawing::Charts::AxisBound::get_ValueAsDate()
```


## Exempel



Visar hur man ställer in anpassade axelgränser.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Rensa diagrammets demodata-serie för att börja med ett rent diagram.
chart->get_Series()->Clear();

// Lägg till en serie med två decimala arrayer. Den första arrayen innehåller X‑värdena,
// och den andra innehåller motsvarande Y‑värden för punkter i spridningsdiagrammet.
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.1, 5.4, 7.9, 3.5, 2.1, 9.7}), System::MakeArray<double>({2.1, 0.3, 0.6, 3.3, 1.4, 1.9}));

// Som standard tillämpas standardskalning på diagrammets X‑ och Y‑axlar,
// så att båda deras intervall är tillräckligt stora för att omfatta varje X‑ och Y‑värde i varje serie.
ASSERT_TRUE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());

// Vi kan definiera våra egna axelgränser.
// I det här fallet kommer vi låta både X‑ och Y‑axelns måttstock visa ett intervall från 0 till 10.
chart->get_AxisX()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(0.0));
chart->get_AxisX()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(10.0));
chart->get_AxisY()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(0.0));
chart->get_AxisY()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(10.0));

ASSERT_FALSE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());
ASSERT_FALSE(chart->get_AxisY()->get_Scaling()->get_Minimum()->get_IsAuto());

// Skapa ett linjediagram med en serie som kräver ett datumintervall på X‑axeln och decimaltal för Y‑axeln.
chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
chart = chartShape->get_Chart();
chart->get_Series()->Clear();

System::ArrayPtr<System::DateTime> dates = System::MakeArray<System::DateTime>({System::DateTime(1973, 5, 11), System::DateTime(1981, 2, 4), System::DateTime(1985, 9, 23), System::DateTime(1989, 6, 28), System::DateTime(1994, 12, 15)});

chart->get_Series()->Add(u"Series 1", dates, System::MakeArray<double>({3.0, 4.7, 5.9, 7.1, 8.9}));

// Vi kan också ange axelgränser i form av datum, vilket begränsar diagrammet till en period.
// Att sätta intervallet till 1980‑1990 kommer att utesluta två av serievärdena
// som ligger utanför intervallet i diagrammet.
chart->get_AxisX()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(1980, 1, 1)));
chart->get_AxisX()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(1990, 1, 1)));

doc->Save(get_ArtifactsDir() + u"Charts.AxisBound.docx");
```

## Se även

* Class [AxisBound](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
