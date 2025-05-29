---
title: ChartMultilevelValue Class
linktitle: ChartMultilevelValue
articleTitle: ChartMultilevelValue
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.ChartMultilevelValue لإدارة البيانات متعددة المستويات في مخططاتك بشكل فعال، مما يعزز قدرات تصور البيانات لديك.
type: docs
weight: 1050
url: /ar/net/aspose.words.drawing.charts/chartmultilevelvalue/
---
## ChartMultilevelValue class

يمثل قيمة للمخططات التي تعرض بيانات متعددة المستويات.

```csharp
public class ChartMultilevelValue
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor)(*string*) | يقوم بتهيئة مثيل جديد لهذه الفئة يمثل قيمة ذات مستوى واحد. |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor_1)(*string, string*) | يقوم بتهيئة مثيل جديد لهذه الفئة يمثل قيمة ذات مستويين. |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor_2)(*string, string, string*) | يقوم بتهيئة مثيل جديد لهذه الفئة يمثل قيمة ثلاثية المستويات. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Level1](../../aspose.words.drawing.charts/chartmultilevelvalue/level1/) { get; } | يحصل على اسم المستوى الأعلى للرسم البياني الذي تشير إليه هذه القيمة. |
| [Level2](../../aspose.words.drawing.charts/chartmultilevelvalue/level2/) { get; } | يحصل على اسم المستوى المتوسط للرسم البياني الذي تشير إليه هذه القيمة. |
| [Level3](../../aspose.words.drawing.charts/chartmultilevelvalue/level3/) { get; } | يحصل على اسم المستوى السفلي للرسم البياني الذي تشير إليه هذه القيمة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/chartmultilevelvalue/equals/)(*object*) | يحصل على علم يشير إلى ما إذا كان الكائن المحدد يساوي كائن البيانات متعدد المستويات الحالي. |
| override [GetHashCode](../../aspose.words.drawing.charts/chartmultilevelvalue/gethashcode/)() | يحصل على رمز تجزئة لكائن البيانات متعدد المستويات الحالي. |

## أمثلة

يوضح كيفية إنشاء مخطط شجرة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//إدراج مخطط شجرة.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

//حذف السلسلة المولدة افتراضيًا.
chart.Series.Clear();

//أضف سلسلة.
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

//إظهار تسميات البيانات.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
