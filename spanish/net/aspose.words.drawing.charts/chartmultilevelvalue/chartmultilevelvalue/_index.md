---
title: ChartMultilevelValue
linktitle: ChartMultilevelValue
articleTitle: ChartMultilevelValue
second_title: Aspose.Words para .NET
description: Descubra el constructor ChartMultilevelValue, diseñado para crear una potente instancia de valor de tres niveles para una mejor visualización y análisis de datos.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.charts/chartmultilevelvalue/chartmultilevelvalue/
---
## ChartMultilevelValue(*string, string, string*) {#constructor_2}

Inicializa una nueva instancia de esta clase que representa un valor de tres niveles.

```csharp
public ChartMultilevelValue(string level1, string level2, string level3)
```

## Ejemplos

Muestra cómo crear un gráfico de mapa de árbol.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un gráfico de mapa de árbol.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

//Eliminar serie generada por defecto.
chart.Series.Clear();

//Añadir una serie.
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

// Mostrar etiquetas de datos.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### Ver también

* class [ChartMultilevelValue](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)

---

## ChartMultilevelValue(*string, string*) {#constructor_1}

Inicializa una nueva instancia de esta clase que representa un valor de dos niveles.

```csharp
public ChartMultilevelValue(string level1, string level2)
```

## Ejemplos

Muestra cómo crear un gráfico de mapa de árbol.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un gráfico de mapa de árbol.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

//Eliminar serie generada por defecto.
chart.Series.Clear();

//Añadir una serie.
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

// Mostrar etiquetas de datos.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### Ver también

* class [ChartMultilevelValue](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)

---

## ChartMultilevelValue(*string*) {#constructor}

Inicializa una nueva instancia de esta clase que representa un valor de un solo nivel.

```csharp
public ChartMultilevelValue(string level1)
```

## Ejemplos

Muestra cómo crear un gráfico de mapa de árbol.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un gráfico de mapa de árbol.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

//Eliminar serie generada por defecto.
chart.Series.Clear();

//Añadir una serie.
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

// Mostrar etiquetas de datos.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### Ver también

* class [ChartMultilevelValue](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
