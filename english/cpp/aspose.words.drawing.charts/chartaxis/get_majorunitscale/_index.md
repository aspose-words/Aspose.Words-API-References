---
title: Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitScale method
linktitle: get_MajorUnitScale
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitScale method. Returns or sets the scale value for major tick marks on the time category axis in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.drawing.charts/chartaxis/get_majorunitscale/
---
## ChartAxis::get_MajorUnitScale method


Returns or sets the scale value for major tick marks on the time category axis.

```cpp
Aspose::Words::Drawing::Charts::AxisTimeUnit Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitScale()
```


## Examples



Shows how to manipulate the tick marks and displayed values of a chart axis. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertChart(ChartType::Scatter, 450, 250);
SharedPtr<Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());

// Set the minor tick marks of the Y-axis to point away from the plot area,
// and the major tick marks to cross the axis.
SharedPtr<ChartAxis> axis = chart->get_AxisY();
axis->set_MajorTickMark(AxisTickMark::Cross);
axis->set_MinorTickMark(AxisTickMark::Outside);

// Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
axis->set_MajorUnit(10);
axis->set_MinorUnit(1);

// Set the Y-axis bounds to -10 and 20.
// This Y-axis will now display 4 major tick marks and 27 minor tick marks.
axis->get_Scaling()->set_Minimum(MakeObject<AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(MakeObject<AxisBound>(20.0));

// For the X-axis, set the major tick marks at every 10 units,
// every minor tick mark at 2.5 units.
axis = chart->get_AxisX();
axis->set_MajorUnit(10);
axis->set_MinorUnit(2.5);

// Configure both types of tick marks to appear inside the graph plot area.
axis->set_MajorTickMark(AxisTickMark::Inside);
axis->set_MinorTickMark(AxisTickMark::Inside);

// Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
axis->get_Scaling()->set_Minimum(MakeObject<AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(MakeObject<AxisBound>(30.0));
axis->set_TickLabelAlignment(ParagraphAlignment::Right);

ASSERT_EQ(1, axis->get_TickLabelSpacing());

// Set the tick labels to display their value in millions.
axis->get_DisplayUnit()->set_Unit(AxisBuiltInUnit::Millions);

// We can set a more specific value by which tick labels will display their values.
// This statement is equivalent to the one above.
axis->get_DisplayUnit()->set_CustomUnit(1000000);

doc->Save(ArtifactsDir + u"Charts.AxisDisplayUnit.docx");
```

## See Also

* Enum [AxisTimeUnit](../../axistimeunit/)
* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
