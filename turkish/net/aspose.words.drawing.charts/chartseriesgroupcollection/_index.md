---
title: ChartSeriesGroupCollection Class
linktitle: ChartSeriesGroupCollection
articleTitle: ChartSeriesGroupCollection
second_title: .NET için Aspose.Words
description: ChartSeriesGroup nesnelerini zahmetsizce yönetmek ve düzenlemek için başvuracağınız çözüm olan Aspose.Words.ChartSeriesGroupCollection sınıfını keşfedin.
type: docs
weight: 1100
url: /tr/net/aspose.words.drawing.charts/chartseriesgroupcollection/
---
## ChartSeriesGroupCollection class

Bir koleksiyonu temsil eder[`ChartSeriesGroup`](../chartseriesgroup/) nesneler.

```csharp
public class ChartSeriesGroupCollection : IEnumerable<ChartSeriesGroup>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriesgroupcollection/count/) { get; } | Bu koleksiyondaki seri gruplarının sayısını döndürür. |
| [Item](../../aspose.words.drawing.charts/chartseriesgroupcollection/item/) { get; } | Bir[`ChartSeriesGroup`](../chartseriesgroup/) belirtilen dizinde. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriesgroupcollection/add/)(*[ChartSeriesType](../chartseriestype/)*) | Bu koleksiyona belirtilen seri türünde yeni bir seri grubu ekler. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriesgroupcollection/getenumerator/)() | Bir numaralandırıcı nesnesi döndürür. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriesgroupcollection/removeat/)(*int*) | Belirtilen dizindeki bir seri grubunu kaldırır. Tüm alt seriler grafikten kaldırılır. |

## Notlar

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafiklerle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) dokümantasyon makalesi.

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

* class [ChartSeriesGroup](../chartseriesgroup/)
* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
