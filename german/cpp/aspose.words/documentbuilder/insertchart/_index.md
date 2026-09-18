---
title: "Aspose::Words::DocumentBuilder::InsertChart Methode"
linktitle: "InsertChart"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertChart Methode. Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe in C++."
type: docs
weight: 30000
url: /de/cpp/aspose.words/documentbuilder/insertchart/
---
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Der Diagrammtyp, der in das Dokument eingefügt werden soll. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| left | double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| top | double | Abstand in Punkten vom Ursprung zur oberen Seite des Bildes. |
| Breite | double | Die Breite des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| Höhe | double | Die Höhe des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| wrapType | Aspose::Words::Drawing::WrapType | Gibt an, wie der Text um das Bild herumfließt. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

## Beispiele



Zeigt, wie man Position und Umbruch beim Einfügen eines Diagramms angibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100, 200, 100, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertedChartRelativePosition.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) method


Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Der Diagrammtyp, der in das Dokument eingefügt werden soll. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| left | double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| top | double | Abstand in Punkten vom Ursprung zur oberen Seite des Bildes. |
| Breite | double | Die Breite des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| Höhe | double | Die Höhe des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| wrapType | Aspose::Words::Drawing::WrapType | Gibt an, wie der Text um das Bild herumfließt. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | Der Stil des eingefügten Diagramms. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

## Siehe auch

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


Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Der Diagrammtyp, der in das Dokument eingefügt werden soll. |
| Breite | double | Die Breite des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| Höhe | double | Die Höhe des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

## Beispiele



Zeigt, wie man ein Kreisdiagramm in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::ConvertUtil::PixelToPoint(300), Aspose::Words::ConvertUtil::PixelToPoint(300))->get_Chart();
chart->get_Series()->Clear();
chart->get_Series()->Add(u"My fruit", System::MakeArray<System::String>({u"Apples", u"Bananas", u"Cherries"}), System::MakeArray<double>({1.3, 2.2, 1.5}));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertPieChart.docx");
```

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) method


Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Der Diagrammtyp, der in das Dokument eingefügt werden soll. |
| Breite | double | Die Breite des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| Höhe | double | Die Höhe des Bildes in Punkten. Kann einen negativen oder null Wert haben, um eine Skalierung von 100 % anzufordern. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | Der Stil des eingefügten Diagramms. |

### ReturnValue

Der Bildknoten, der gerade eingefügt wurde.
## Hinweise


Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem [Shape](../../../aspose.words.drawing/shape/) Objekt ändern, das von dieser Methode zurückgegeben wird.

## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
