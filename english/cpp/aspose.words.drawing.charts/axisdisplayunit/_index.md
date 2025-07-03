---
title: Aspose::Words::Drawing::Charts::AxisDisplayUnit class
linktitle: AxisDisplayUnit
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::AxisDisplayUnit class. Provides access to the scaling options of the display units for the value axis. To learn more, visit the  documentation article in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.drawing.charts/axisdisplayunit/
---
## AxisDisplayUnit class


Provides access to the scaling options of the display units for the value axis. To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article.

```cpp
class AxisDisplayUnit : public Aspose::Words::Drawing::Charts::Core::IDmlChartTitleHolder,
                        public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## Methods

| Method | Description |
| --- | --- |
| [AxisDisplayUnit](./axisdisplayunit/)() |  |
| [get_CustomUnit](./get_customunit/)() const | Gets or sets a user-defined divisor to scale display units on the value axis. |
| [get_Document](./get_document/)() | Returns the document containing the parent chart. |
| [get_Unit](./get_unit/)() const | Gets or sets the scaling value of the display units as one of the predefined values. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CustomUnit](./set_customunit/)(double) | Setter for [Aspose::Words::Drawing::Charts::AxisDisplayUnit::get_CustomUnit](./get_customunit/). |
| [set_Unit](./set_unit/)(Aspose::Words::Drawing::Charts::AxisBuiltInUnit) | Setter for [Aspose::Words::Drawing::Charts::AxisDisplayUnit::get_Unit](./get_unit/). |
| static [Type](./type/)() |  |

## Examples



Shows how to manipulate the tick marks and displayed values of a chart axis. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());

// Set the minor tick marks of the Y-axis to point away from the plot area,
// and the major tick marks to cross the axis.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisY();
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);

// Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
axis->set_MajorUnit(10);
axis->set_MinorUnit(1);

// Set the Y-axis bounds to -10 and 20.
// This Y-axis will now display 4 major tick marks and 27 minor tick marks.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(20.0));

// For the X-axis, set the major tick marks at every 10 units,
// every minor tick mark at 2.5 units.
axis = chart->get_AxisX();
axis->set_MajorUnit(10);
axis->set_MinorUnit(2.5);

// Configure both types of tick marks to appear inside the graph plot area.
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);

// Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(30.0));
axis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

ASSERT_EQ(1, axis->get_TickLabels()->get_Spacing());
ASPOSE_ASSERT_EQ(doc, axis->get_DisplayUnit()->get_Document());

// Set the tick labels to display their value in millions.
axis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Millions);

// We can set a more specific value by which tick labels will display their values.
// This statement is equivalent to the one above.
axis->get_DisplayUnit()->set_CustomUnit(1000000);

doc->Save(get_ArtifactsDir() + u"Charts.AxisDisplayUnit.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
