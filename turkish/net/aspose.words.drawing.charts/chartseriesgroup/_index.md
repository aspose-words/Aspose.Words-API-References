---
title: ChartSeriesGroup Class
linktitle: ChartSeriesGroup
articleTitle: ChartSeriesGroup
second_title: .NET için Aspose.Words
description: Gelişmiş veri görselleştirme ve analizi için grafik serisi özelliklerini yönetmeyi basitleştiren Aspose.Words.Drawing.Charts.ChartSeriesGroup sınıfını keşfedin.
type: docs
weight: 1090
url: /tr/net/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class

Bir grafik serisi grubunun özelliklerini, yani aynı eksenlerle ilişkili aynı türdeki grafik serisinin özelliklerini temsil eder.

```csharp
public class ChartSeriesGroup
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AxisGroup](../../aspose.words.drawing.charts/chartseriesgroup/axisgroup/) { get; set; } | Bu seri grubunun ait olduğu eksen grubunu alır veya ayarlar. |
| [AxisX](../../aspose.words.drawing.charts/chartseriesgroup/axisx/) { get; } | Bu seri grubunun X ekseninin özelliklerine erişim sağlar. |
| [AxisY](../../aspose.words.drawing.charts/chartseriesgroup/axisy/) { get; } | Bu seri grubunun Y ekseninin özelliklerine erişim sağlar. |
| [BubbleScale](../../aspose.words.drawing.charts/chartseriesgroup/bubblescale/) { get; set; } | Kabarcıkların boyutunu varsayılan boyutlarının yüzdesi olarak alır veya ayarlar. |
| [DoughnutHoleSize](../../aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/) { get; set; } | Ana halka grafiğinin delik boyutunu yüzde olarak alır veya ayarlar. |
| [FirstSliceAngle](../../aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/) { get; set; } | Ana pasta grafiğinin ilk diliminin açısını derece olarak alır veya ayarlar. |
| [GapWidth](../../aspose.words.drawing.charts/chartseriesgroup/gapwidth/) { get; set; } | Grafik öğeleri arasındaki boşluk genişliğinin yüzdesini alır veya ayarlar. |
| [Overlap](../../aspose.words.drawing.charts/chartseriesgroup/overlap/) { get; set; } | Seri çubuklarının veya sütunlarının ne kadar örtüştüğünün yüzdesini alır veya ayarlar. |
| [SecondSectionSize](../../aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/) { get; set; } | Pasta grafiğinin ikincil bölümünün boyutunu yüzde olarak alır veya ayarlar. |
| [Series](../../aspose.words.drawing.charts/chartseriesgroup/series/) { get; } | Bu seri grubuna ait serilerin bir koleksiyonunu alır. |
| [SeriesType](../../aspose.words.drawing.charts/chartseriesgroup/seriestype/) { get; } | Bu grupta yer alan grafik serisinin türünü alır. |

## Notlar

Kombo grafikler, her seri türü için ayrı bir grup bulunan birden fazla grafik serisi grubu içerir.

Ayrıca, bir veya daha fazla grafik serisine ikincil eksenler atamak için bir grafik serisi grubu oluşturabilirsiniz.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[ Grafiklerle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) belgeleme makalesi.

## Örnekler

Grafikte ikincil eksenle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 250);
Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;

// Varsayılan olarak oluşturulan seriyi sil.
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
series.Add("Series 1 of primary series group", categories, new double[] { 2, 3, 4 });
series.Add("Series 2 of primary series group", categories, new double[] { 5, 2, 3 });

// Satır tipinde ek bir seri grubu oluştur.
ChartSeriesGroup newSeriesGroup = chart.SeriesGroups.Add(ChartSeriesType.Line);
// Yeni seri grubu için ikincil eksenlerin kullanımını belirtin.
newSeriesGroup.AxisGroup = AxisGroup.Secondary;
// İkincil X eksenini gizle.
newSeriesGroup.AxisX.Hidden = true;
// İkincil Y ekseninin başlığını tanımlayın.
newSeriesGroup.AxisY.Title.Show = true;
newSeriesGroup.AxisY.Title.Text = "Secondary Y axis";

Assert.AreEqual(ChartSeriesType.Line, newSeriesGroup.SeriesType);

// Yeni seri grubuna bir seri ekle.
ChartSeries series3 =
    newSeriesGroup.Series.Add("Series of secondary series group", categories, new double[] { 13, 11, 16 });
series3.Format.Stroke.Weight = 3.5;

doc.Save(ArtifactsDir + "Charts.SecondaryAxis.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
