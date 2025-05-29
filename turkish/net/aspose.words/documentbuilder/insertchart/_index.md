---
title: DocumentBuilder.InsertChart
linktitle: InsertChart
articleTitle: InsertChart
second_title: .NET için Aspose.Words
description: DocumentBuilder InsertChart yöntemiyle belgelerinizi zahmetsizce geliştirin. Etkili sunumlar için grafik nesnelerini sorunsuzca ekleyin ve yeniden boyutlandırın.
type: docs
weight: 280
url: /tr/net/aspose.words/documentbuilder/insertchart/
---
## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), double, double*) {#insertchart_2}

Belgeye bir grafik nesnesi ekler ve belirtilen boyuta ölçekler.

```csharp
public Shape InsertChart(ChartType chartType, double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| chartType | ChartType | Belgeye eklenecek grafik türü. |
| width | Double | Resmin noktalardaki genişliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |
| height | Double | Resmin nokta cinsinden yüksekliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |

### Geri dönüş değeri

Az önce eklenen görüntü düğümü.

## Notlar

kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu metot tarafından döndürülen nesne.

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

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), double, double, [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)*) {#insertchart_3}

Belgeye bir grafik nesnesi ekler ve belirtilen boyuta ölçekler.

```csharp
public Shape InsertChart(ChartType chartType, double width, double height, ChartStyle chartStyle)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| chartType | ChartType | Belgeye eklenecek grafik türü. |
| width | Double | Resmin noktalardaki genişliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |
| height | Double | Resmin nokta cinsinden yüksekliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |
| chartStyle | ChartStyle | Eklenen grafiğin stili. |

### Geri dönüş değeri

Az önce eklenen görüntü düğümü.

## Notlar

kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu metot tarafından döndürülen nesne.

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertchart}

Belgeye bir grafik nesnesi ekler ve belirtilen boyuta ölçekler.

```csharp
public Shape InsertChart(ChartType chartType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| chartType | ChartType | Belgeye eklenecek grafik türü. |
| horzPos | RelativeHorizontalPosition | Görüntüye olan mesafenin nereden ölçüleceğini belirtir. |
| left | Double | Görüntünün başlangıç noktasından sol tarafa kadar olan mesafe. |
| vertPos | RelativeVerticalPosition | Görüntüye olan mesafenin nereden ölçüleceğini belirtir. |
| top | Double | Görüntünün başlangıç noktasından üst tarafına kadar olan mesafenin nokta cinsinden ifadesi. |
| width | Double | Resmin noktalardaki genişliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |
| height | Double | Resmin nokta cinsinden yüksekliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |
| wrapType | WrapType | Metnin resmin etrafına nasıl sarılacağını belirtir. |

### Geri dönüş değeri

Az önce eklenen görüntü düğümü.

## Notlar

kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu metot tarafından döndürülen nesne.

## Örnekler

Bir grafik eklerken konum ve sarmanın nasıl belirleneceğini gösterir.

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

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/), [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)*) {#insertchart_1}

Belgeye bir grafik nesnesi ekler ve belirtilen boyuta ölçekler.

```csharp
public Shape InsertChart(ChartType chartType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType, 
    ChartStyle chartStyle)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| chartType | ChartType | Belgeye eklenecek grafik türü. |
| horzPos | RelativeHorizontalPosition | Görüntüye olan mesafenin nereden ölçüleceğini belirtir. |
| left | Double | Görüntünün başlangıç noktasından sol tarafa kadar olan mesafe. |
| vertPos | RelativeVerticalPosition | Görüntüye olan mesafenin nereden ölçüleceğini belirtir. |
| top | Double | Görüntünün başlangıç noktasından üst tarafına kadar olan mesafenin nokta cinsinden ifadesi. |
| width | Double | Resmin noktalardaki genişliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |
| height | Double | Resmin nokta cinsinden yüksekliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |
| wrapType | WrapType | Metnin resmin etrafına nasıl sarılacağını belirtir. |
| chartStyle | ChartStyle | Eklenen grafiğin stili. |

### Geri dönüş değeri

Az önce eklenen görüntü düğümü.

## Notlar

kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu metot tarafından döndürülen nesne.

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
