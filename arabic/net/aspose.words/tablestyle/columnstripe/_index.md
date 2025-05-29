---
title: TableStyle.ColumnStripe
linktitle: ColumnStripe
articleTitle: ColumnStripe
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية TableStyle ColumnStripe لتخصيص نطاقات الأعمدة الفردية/الزوجية بسهولة للحصول على مظهر أنيق واحترافي في جداولك.
type: docs
weight: 70
url: /ar/net/aspose.words/tablestyle/columnstripe/
---
## TableStyle.ColumnStripe property

يحصل على أو يعين عددًا من الأعمدة المراد تضمينها في النطاق عندما يحدد النمط نطاق الأعمدة الفردية/الزوجية.

```csharp
public int ColumnStripe { get; set; }
```

## أمثلة

يوضح كيفية إنشاء أنماط جدول مشروطة تتناوب بين الصفوف.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكننا تكوين نمط مشروط للجدول لتطبيق لون مختلف على الصف/العمود،
// بناءً على ما إذا كان الصف/العمود زوجيًا أو فرديًا، يتم إنشاء نمط ألوان متناوب.
// يمكننا أيضًا تطبيق رقم n على شريط الصف/العمود،
// وهذا يعني أن اللون يتناوب بعد كل n صف/عمود بدلاً من واحد.
// قم بإنشاء جدول حيث سيتم تقسيم الأعمدة والصفوف الفردية إلى مجموعات ثلاثية.
Table table = builder.StartTable();
for (int i = 0; i < 15; i++)
{
    for (int j = 0; j < 4; j++)
    {
        builder.InsertCell();
        builder.Writeln($"{(j % 2 == 0 ? "Even" : "Odd")} column.");
        builder.Write($"Row banding {(i % 3 == 0 ? "start" : "continuation")}.");
    }
    builder.EndRow();
}
builder.EndTable();

// تطبيق نمط الخط على كافة حدود الجدول.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Double;

// قم بتعيين اللونين، اللذين سيتم تبديلهما كل 3 صفوف.
tableStyle.RowStripe = 3;
tableStyle.ConditionalStyles[ConditionalStyleType.OddRowBanding].Shading.BackgroundPatternColor = Color.LightBlue;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenRowBanding].Shading.BackgroundPatternColor = Color.LightCyan;

// تعيين لون لتطبيقه على كل عمود زوجي، والذي سيحل محل أي تلوين صف مخصص.
tableStyle.ColumnStripe = 1;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenColumnBanding].Shading.BackgroundPatternColor = Color.LightSalmon;

table.Style = tableStyle;

// تعمل خاصية "StyleOptions" على تمكين تقسيم الصفوف بشكل افتراضي.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands,
    table.StyleOptions);

// استخدم خاصية "StyleOptions" أيضًا لتمكين تقسيم الأعمدة.
table.StyleOptions = table.StyleOptions | TableStyleOptions.ColumnBands;

doc.Save(ArtifactsDir + "Table.AlternatingRowStyles.docx");
```

### أنظر أيضا

* class [TableStyle](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
