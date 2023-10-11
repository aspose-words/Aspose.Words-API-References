---
title: DocumentBuilder.InsertChart
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe.
type: docs
weight: 280
url: /de/net/aspose.words/documentbuilder/insertchart/
---
## InsertChart(ChartType, double, double) {#insertchart_1}

Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertChart(ChartType chartType, double width, double height)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartType | ChartType | Der Diagrammtyp, der in das Dokument eingefügt werden soll. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

### Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern[`Shape`](../../../aspose.words.drawing/shape/) Von dieser Methode zurückgegebenes Objekt.

### Beispiele

Zeigt, wie man ein Kreisdiagramm in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, ConvertUtil.PixelToPoint(300), 
    ConvertUtil.PixelToPoint(300)).Chart;
chart.Series.Clear();
chart.Series.Add("My fruit",
    new[] { "Apples", "Bananas", "Cherries" },
    new[] { 1.3, 2.2, 1.5 });

doc.Save(ArtifactsDir + "DocumentBuilder.InsertPieChart.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)

---

## InsertChart(ChartType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertchart}

Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertChart(ChartType chartType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartType | ChartType | Der Diagrammtyp, der in das Dokument eingefügt werden soll. |
| horzPos | RelativeHorizontalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | RelativeVerticalPosition | Gibt an, von wo aus der Abstand zum Bild gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung zur oberen Seite des Bildes. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer Wert oder ein Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| wrapType | WrapType | Gibt an, wie Text um das Bild herum umbrochen wird. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

### Bemerkungen

Sie können die Bildgröße, Position, Positionierungsmethode und andere Einstellungen mit dem ändern[`Shape`](../../../aspose.words.drawing/shape/) Von dieser Methode zurückgegebenes Objekt.

### Beispiele

Zeigt, wie man beim Einfügen eines Diagramms Position und Umbruch angibt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertChart(ChartType.Pie, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
    100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertedChartRelativePosition.docx");
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


