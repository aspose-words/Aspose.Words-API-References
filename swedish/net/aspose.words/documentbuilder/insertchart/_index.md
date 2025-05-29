---
title: DocumentBuilder.InsertChart
linktitle: InsertChart
articleTitle: InsertChart
second_title: Aspose.Words för .NET
description: Förbättra dina dokument enkelt med DocumentBuilder InsertChart-metoden. Lägg till och ändra storlek på diagramobjekt sömlöst för effektfulla presentationer.
type: docs
weight: 280
url: /sv/net/aspose.words/documentbuilder/insertchart/
---
## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), double, double*) {#insertchart_2}

Infogar ett diagramobjekt i dokumentet och skalar det till den angivna storleken.

```csharp
public Shape InsertChart(ChartType chartType, double width, double height)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| chartType | ChartType | Diagramtypen som ska infogas i dokumentet. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

## Exempel

Visar hur man infogar ett cirkeldiagram i ett dokument.

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

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), double, double, [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)*) {#insertchart_3}

Infogar ett diagramobjekt i dokumentet och skalar det till den angivna storleken.

```csharp
public Shape InsertChart(ChartType chartType, double width, double height, ChartStyle chartStyle)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| chartType | ChartType | Diagramtypen som ska infogas i dokumentet. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| chartStyle | ChartStyle | Stilen för det infogade diagrammet. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertchart}

Infogar ett diagramobjekt i dokumentet och skalar det till den angivna storleken.

```csharp
public Shape InsertChart(ChartType chartType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| chartType | ChartType | Diagramtypen som ska infogas i dokumentet. |
| horzPos | RelativeHorizontalPosition | Anger varifrån avståndet till bilden mäts. |
| left | Double | Avstånd i punkter från origo till bildens vänstra sida. |
| vertPos | RelativeVerticalPosition | Anger varifrån avståndet till bilden mäts. |
| top | Double | Avstånd i punkter från origo till bildens översida. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| wrapType | WrapType | Anger hur text ska radbrytas runt bilden. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

## Exempel

Visar hur man anger position och radbrytning när man infogar ett diagram.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertChart(ChartType.Pie, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
    100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertedChartRelativePosition.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/), [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)*) {#insertchart_1}

Infogar ett diagramobjekt i dokumentet och skalar det till den angivna storleken.

```csharp
public Shape InsertChart(ChartType chartType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType, 
    ChartStyle chartStyle)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| chartType | ChartType | Diagramtypen som ska infogas i dokumentet. |
| horzPos | RelativeHorizontalPosition | Anger varifrån avståndet till bilden mäts. |
| left | Double | Avstånd i punkter från origo till bildens vänstra sida. |
| vertPos | RelativeVerticalPosition | Anger varifrån avståndet till bilden mäts. |
| top | Double | Avstånd i punkter från origo till bildens översida. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| wrapType | WrapType | Anger hur text ska radbrytas runt bilden. |
| chartStyle | ChartStyle | Stilen för det infogade diagrammet. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
