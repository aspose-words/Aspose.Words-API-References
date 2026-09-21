---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitScale metod"
linktitle: "get_MinorUnitScale"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitScale metod. Returnerar eller anger skalan för mindre tickmarkeringar på tidskategorins axel i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words.drawing.charts/chartaxis/get_minorunitscale/
---
## ChartAxis::get_MinorUnitScale method


Returnerar eller anger skalvärdet för sekundära tick‑markeringar på tidskategori‑axeln.

```cpp
Aspose::Words::Drawing::Charts::AxisTimeUnit Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitScale()
```


## Exempel



Visar hur man manipulerar tick-markeringarna och de visade värdena för en diagramaxel.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());

// Ställ in de mindre tick-markeringarna på Y-axeln så att de pekar bort från plotområdet,
// och de större tick-markeringarna så att de korsar axeln.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisY();
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);

// Ställ in Y-axeln så att den visar en huvudtick var 10 enheter och en mindre tick var 1 enhet.
axis->set_MajorUnit(10);
axis->set_MinorUnit(1);

// Ställ in Y-axelns gränser till -10 och 20.
// Denna Y-axel kommer nu att visa 4 stora tick-markeringar och 27 mindre tick-markeringar.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(20.0));

// För X-axeln, ställ in de stora tick-markeringarna var 10 enhet,
// varje mindre tick-markering var 2,5 enhet.
axis = chart->get_AxisX();
axis->set_MajorUnit(10);
axis->set_MinorUnit(2.5);

// Konfigurera båda typerna av tick-markeringar så att de visas inom diagrammets plotområde.
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);

// Ställ in X-axelns gränser så att X-axeln omfattar 5 stora tick-markeringar och 12 mindre tick-markeringar.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(30.0));
axis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

ASSERT_EQ(1, axis->get_TickLabels()->get_Spacing());
ASPOSE_ASSERT_EQ(doc, axis->get_DisplayUnit()->get_Document());

// Ställ in tick-etiketterna så att de visar sitt värde i miljoner.
axis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Millions);

// Vi kan ange ett mer specifikt värde som tick-etiketterna ska visa sina värden med.
// Detta påstående är ekvivalent med det ovanstående.
axis->get_DisplayUnit()->set_CustomUnit(1000000);

doc->Save(get_ArtifactsDir() + u"Charts.AxisDisplayUnit.docx");
```

## Se även

* Enum [AxisTimeUnit](../../axistimeunit/)
* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
