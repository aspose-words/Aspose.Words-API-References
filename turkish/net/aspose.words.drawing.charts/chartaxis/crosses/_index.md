---
title: ChartAxis.Crosses
second_title: Aspose.Words for .NET API Referansı
description: ChartAxis mülk. Bu eksenin dikey ekseni nasıl kestiğini belirtir.
type: docs
weight: 40
url: /tr/net/aspose.words.drawing.charts/chartaxis/crosses/
---
## ChartAxis.Crosses property

Bu eksenin dikey ekseni nasıl kestiğini belirtir.

```csharp
public AxisCrosses Crosses { get; set; }
```

### Notlar

Varsayılan değer:Automatic.

Bu özellik MS Office 2016 yeni çizelgeleri tarafından desteklenmemektedir.

### Örnekler

Grafiğin nasıl ekleneceğini ve eksenlerinin görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// X ekseni için kategorileri ve Y ekseni için ilgili sayısal değerleri içeren bir grafik serisi ekleyin.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Grafik eksenlerinin görünümlerini değiştirebilecek çeşitli seçenekleri vardır,
// yönleri, büyük/küçük birim işaretleri ve onay işaretleri gibi.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabelOffset = 50;
xAxis.TickLabelPosition = AxisTickLabelPosition.Low;
xAxis.TickLabelSpacingIsAuto = false;
xAxis.TickMarkSpacing = 1;

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabelPosition = AxisTickLabelPosition.NextToAxis;

// Sütun grafiklerinde Z ekseni yoktur.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Ayrıca bakınız

* enum [AxisCrosses](../../axiscrosses/)
* class [ChartAxis](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartaxis/)
* toplantı [Aspose.Words](../../../)


