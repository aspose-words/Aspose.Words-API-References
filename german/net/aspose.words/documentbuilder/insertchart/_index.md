---
title: DocumentBuilder.InsertChart
linktitle: InsertChart
articleTitle: InsertChart
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Dokumente mühelos mit der InsertChart-Methode von DocumentBuilder. Fügen Sie Diagrammobjekte nahtlos hinzu und passen Sie deren Größe an, um wirkungsvolle Präsentationen zu erstellen.
type: docs
weight: 280
url: /de/net/aspose.words/documentbuilder/insertchart/
---
## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), double, double*) {#insertchart_2}

Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertChart(ChartType chartType, double width, double height)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartType | ChartType | Der in das Dokument einzufügende Diagrammtyp. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie ein Kreisdiagramm in ein Dokument eingefügt wird.

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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), double, double, [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)*) {#insertchart_3}

Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertChart(ChartType chartType, double width, double height, ChartStyle chartStyle)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartType | ChartType | Der in das Dokument einzufügende Diagrammtyp. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| chartStyle | ChartStyle | Der Stil des eingefügten Diagramms. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertchart}

Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertChart(ChartType chartType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartType | ChartType | Der in das Dokument einzufügende Diagrammtyp. |
| horzPos | RelativeHorizontalPosition | Gibt an, von wo aus die Entfernung zum Bild gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | RelativeVerticalPosition | Gibt an, von wo aus die Entfernung zum Bild gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung zur oberen Bildseite. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| wrapType | WrapType | Gibt an, wie der Text um das Bild herumfließen soll. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

## Beispiele

Zeigt, wie Sie beim Einfügen eines Diagramms Position und Umbruch angeben.

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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/), [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)*) {#insertchart_1}

Fügt ein Diagrammobjekt in das Dokument ein und skaliert es auf die angegebene Größe.

```csharp
public Shape InsertChart(ChartType chartType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType, 
    ChartStyle chartStyle)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartType | ChartType | Der in das Dokument einzufügende Diagrammtyp. |
| horzPos | RelativeHorizontalPosition | Gibt an, von wo aus die Entfernung zum Bild gemessen wird. |
| left | Double | Abstand in Punkten vom Ursprung zur linken Seite des Bildes. |
| vertPos | RelativeVerticalPosition | Gibt an, von wo aus die Entfernung zum Bild gemessen wird. |
| top | Double | Abstand in Punkten vom Ursprung zur oberen Bildseite. |
| width | Double | Die Breite des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| height | Double | Die Höhe des Bildes in Punkten. Kann ein negativer oder Nullwert sein, um eine Skalierung von 100 % anzufordern. |
| wrapType | WrapType | Gibt an, wie der Text um das Bild herumfließen soll. |
| chartStyle | ChartStyle | Der Stil des eingefügten Diagramms. |

### Rückgabewert

Der Bildknoten, der gerade eingefügt wurde.

## Bemerkungen

Sie können die Bildgröße, den Speicherort, die Positionierungsmethode und andere Einstellungen mit dem ändern.[`Shape`](../../../aspose.words.drawing/shape/) von dieser Methode zurückgegebenes Objekt.

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
