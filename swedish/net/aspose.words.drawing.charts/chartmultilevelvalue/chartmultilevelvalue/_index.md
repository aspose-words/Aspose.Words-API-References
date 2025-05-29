---
title: ChartMultilevelValue
linktitle: ChartMultilevelValue
articleTitle: ChartMultilevelValue
second_title: Aspose.Words för .NET
description: Upptäck konstruktorn ChartMultilevelValue, utformad för att skapa en kraftfull värdeinstans med tre nivåer för förbättrad datavisualisering och analys.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.charts/chartmultilevelvalue/chartmultilevelvalue/
---
## ChartMultilevelValue(*string, string, string*) {#constructor_2}

Initierar en ny instans av den här klassen som representerar ett värde med tre nivåer.

```csharp
public ChartMultilevelValue(string level1, string level2, string level3)
```

## Exempel

Visar hur man skapar ett trädkartdiagram.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett trädkartdiagram.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

// Radera standardgenererad serie.
chart.Series.Clear();

// Lägg till en serie.
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

// Visa dataetiketter.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### Se även

* class [ChartMultilevelValue](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)

---

## ChartMultilevelValue(*string, string*) {#constructor_1}

Initierar en ny instans av den här klassen som representerar ett värde med två nivåer.

```csharp
public ChartMultilevelValue(string level1, string level2)
```

## Exempel

Visar hur man skapar ett trädkartdiagram.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett trädkartdiagram.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

// Radera standardgenererad serie.
chart.Series.Clear();

// Lägg till en serie.
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

// Visa dataetiketter.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### Se även

* class [ChartMultilevelValue](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)

---

## ChartMultilevelValue(*string*) {#constructor}

Initierar en ny instans av den här klassen som representerar ett värde på en nivå.

```csharp
public ChartMultilevelValue(string level1)
```

## Exempel

Visar hur man skapar ett trädkartdiagram.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett trädkartdiagram.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

// Radera standardgenererad serie.
chart.Series.Clear();

// Lägg till en serie.
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

// Visa dataetiketter.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### Se även

* class [ChartMultilevelValue](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
