---
title: DocumentBuilder.InsertChart
linktitle: InsertChart
articleTitle: InsertChart
second_title: Aspose.Words for .NET
description: DocumentBuilder InsertChart yöntem. Belgeye bir grafik nesnesi ekler ve bunu belirtilen boyuta ölçeklendirir C#'da.
type: docs
weight: 280
url: /tr/net/aspose.words/documentbuilder/insertchart/
---
## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), double, double*) {#insertchart_1}

Belgeye bir grafik nesnesi ekler ve bunu belirtilen boyuta ölçeklendirir.

```csharp
public Shape InsertChart(ChartType chartType, double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| chartType | ChartType | Belgeye eklenecek grafik türü. |
| width | Double | Nokta cinsinden görüntünün genişliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |
| height | Double | Nokta cinsinden görüntünün yüksekliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

## Notlar

'yi kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

## Örnekler

Bir belgeye pasta grafiğinin nasıl ekleneceğini gösterir.

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

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertchart}

Belgeye bir grafik nesnesi ekler ve bunu belirtilen boyuta ölçeklendirir.

```csharp
public Shape InsertChart(ChartType chartType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| chartType | ChartType | Belgeye eklenecek grafik türü. |
| horzPos | RelativeHorizontalPosition | Görüntüye olan mesafenin nereden ölçüleceğini belirtir. |
| left | Double | Nokta cinsinden görüntünün başlangıç noktasından sol tarafına olan uzaklık. |
| vertPos | RelativeVerticalPosition | Görüntüye olan mesafenin nereden ölçüldüğünü belirtir. |
| top | Double | Orijinden görüntünün üst kısmına kadar olan nokta cinsinden uzaklık. |
| width | Double | Nokta cinsinden görüntünün genişliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |
| height | Double | Nokta cinsinden görüntünün yüksekliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |
| wrapType | WrapType | Metnin görüntünün etrafına nasıl sarılacağını belirtir. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

## Notlar

'yi kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

## Örnekler

Grafik eklerken konumun ve sarmanın nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertChart(ChartType.Pie, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
    100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertedChartRelativePosition.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
