---
title: ChartMultilevelValue Class
linktitle: ChartMultilevelValue
articleTitle: ChartMultilevelValue
second_title: .NET için Aspose.Words
description: Grafiklerinizdeki çok düzeyli verileri etkili bir şekilde yönetmek ve veri görselleştirme yeteneklerinizi geliştirmek için Aspose.Words.ChartMultilevelValue sınıfını keşfedin.
type: docs
weight: 1050
url: /tr/net/aspose.words.drawing.charts/chartmultilevelvalue/
---
## ChartMultilevelValue class

Çok düzeyli verileri görüntüleyen grafikler için bir değeri temsil eder.

```csharp
public class ChartMultilevelValue
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor)(*string*) | Bu sınıfın tek düzeyli bir değeri temsil eden yeni bir örneğini başlatır. |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor_1)(*string, string*) | Bu sınıfın iki düzeyli bir değeri temsil eden yeni bir örneğini başlatır. |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor_2)(*string, string, string*) | Bu sınıfın üç seviyeli bir değeri temsil eden yeni bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Level1](../../aspose.words.drawing.charts/chartmultilevelvalue/level1/) { get; } | Bu değerin başvurduğu grafik üst düzeyinin adını alır. |
| [Level2](../../aspose.words.drawing.charts/chartmultilevelvalue/level2/) { get; } | Bu değerin başvurduğu grafik ara düzeyinin adını alır. |
| [Level3](../../aspose.words.drawing.charts/chartmultilevelvalue/level3/) { get; } | Bu değerin başvurduğu grafik alt seviyesinin adını alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/chartmultilevelvalue/equals/)(*object*) | Belirtilen nesnenin geçerli çok düzeyli veri nesnesine eşit olup olmadığını gösteren bir bayrak alır. |
| override [GetHashCode](../../aspose.words.drawing.charts/chartmultilevelvalue/gethashcode/)() | Mevcut çok düzeyli veri nesnesi için bir karma kodu alır. |

## Örnekler

Ağaç haritası grafiğinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir Treemap grafiği ekle.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

// Varsayılan olarak oluşturulan seriyi sil.
chart.Series.Clear();

// Bir seri ekle.
ChartSeries series = chart.Series.Add(
    "Population by Region",
    new ChartMultilevelValue[]
    {
        new ChartMultilevelValue("Asia", "China"),
        new ChartMultilevelValue("Asia", "India"),
        new ChartMultilevelValue("Asia", "Indonesia"),
        new ChartMultilevelValue("Asia", "Pakistan"),
        new ChartMultilevelValue("Asia", "Bangladesh"),
        new ChartMultilevelValue("Asia", "Japan"),
        new ChartMultilevelValue("Asia", "Philippines"),
        new ChartMultilevelValue("Asia", "Other"),
        new ChartMultilevelValue("Africa", "Nigeria"),
        new ChartMultilevelValue("Africa", "Ethiopia"),
        new ChartMultilevelValue("Africa", "Egypt"),
        new ChartMultilevelValue("Africa", "Other"),
        new ChartMultilevelValue("Europe", "Russia"),
        new ChartMultilevelValue("Europe", "Germany"),
        new ChartMultilevelValue("Europe", "Other"),
        new ChartMultilevelValue("Latin America", "Brazil"),
        new ChartMultilevelValue("Latin America", "Mexico"),
        new ChartMultilevelValue("Latin America", "Other"),
        new ChartMultilevelValue("Northern America", "United States", "Other"),
        new ChartMultilevelValue("Northern America", "Other"),
        new ChartMultilevelValue("Oceania")
    },
    new double[]
    {
        1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000,
        223800000, 107334000, 105914499, 903000000,
        146150789, 84607016, 516000000,
        203080756, 129713690, 310000000,
        335893238, 35000000,
        42000000
    });

// Veri etiketlerini göster.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
