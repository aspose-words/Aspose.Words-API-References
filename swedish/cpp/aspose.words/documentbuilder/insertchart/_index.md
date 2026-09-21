---
title: "Aspose::Words::DocumentBuilder::InsertChart metod"
linktitle: "InsertChart"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::InsertChart metod. Infogar ett diagramobjekt i dokumentet och skalar det till den angivna storleken i C++."
type: docs
weight: 30000
url: /sv/cpp/aspose.words/documentbuilder/insertchart/
---
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Infogar ett diagramobjekt i dokumentet och skalar det till angiven storlek.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Diagramtypen som ska infogas i dokumentet. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Anger var avståndet till bilden mäts från. |
| left | double | Avstånd i punkter från ursprunget till bildens vänstra sida. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Anger var avståndet till bilden mäts från. |
| top | double | Avstånd i punkter från ursprunget till bildens övre sida. |
| bredd | double | Bredden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| höjd | double | Höjden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| wrapType | Aspose::Words::Drawing::WrapType | Anger hur text ska omslutas runt bilden. |

### ReturnValue

Bildnod som just har infogats.
## Anmärkningar


Du kan ändra bildens storlek, plats, placeringsmetod och andra inställningar med hjälp av objektet [Shape](../../../aspose.words.drawing/shape/) som returneras av denna metod.

## Exempel



Visar hur man anger position och omslag när man infogar ett diagram.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100, 200, 100, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertedChartRelativePosition.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) method


Infogar ett diagramobjekt i dokumentet och skalar det till angiven storlek.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Diagramtypen som ska infogas i dokumentet. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Anger var avståndet till bilden mäts från. |
| left | double | Avstånd i punkter från ursprunget till bildens vänstra sida. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Anger var avståndet till bilden mäts från. |
| top | double | Avstånd i punkter från ursprunget till bildens övre sida. |
| bredd | double | Bredden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| höjd | double | Höjden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| wrapType | Aspose::Words::Drawing::WrapType | Anger hur text ska omslutas runt bilden. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | Stilen på det infogade diagrammet. |

### ReturnValue

Bildnod som just har infogats.
## Anmärkningar


Du kan ändra bildens storlek, plats, placeringsmetod och andra inställningar med hjälp av objektet [Shape](../../../aspose.words.drawing/shape/) som returneras av denna metod.

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, double, double) method


Infogar ett diagramobjekt i dokumentet och skalar det till angiven storlek.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Diagramtypen som ska infogas i dokumentet. |
| bredd | double | Bredden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| höjd | double | Höjden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |

### ReturnValue

Bildnod som just har infogats.
## Anmärkningar


Du kan ändra bildens storlek, plats, placeringsmetod och andra inställningar med hjälp av objektet [Shape](../../../aspose.words.drawing/shape/) som returneras av denna metod.

## Exempel



Visar hur man infogar ett cirkeldiagram i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::ConvertUtil::PixelToPoint(300), Aspose::Words::ConvertUtil::PixelToPoint(300))->get_Chart();
chart->get_Series()->Clear();
chart->get_Series()->Add(u"My fruit", System::MakeArray<System::String>({u"Apples", u"Bananas", u"Cherries"}), System::MakeArray<double>({1.3, 2.2, 1.5}));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertPieChart.docx");
```

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) method


Infogar ett diagramobjekt i dokumentet och skalar det till angiven storlek.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Diagramtypen som ska infogas i dokumentet. |
| bredd | double | Bredden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| höjd | double | Höjden på bilden i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | Stilen på det infogade diagrammet. |

### ReturnValue

Bildnod som just har infogats.
## Anmärkningar


Du kan ändra bildens storlek, plats, placeringsmetod och andra inställningar med hjälp av objektet [Shape](../../../aspose.words.drawing/shape/) som returneras av denna metod.

## Se även

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
