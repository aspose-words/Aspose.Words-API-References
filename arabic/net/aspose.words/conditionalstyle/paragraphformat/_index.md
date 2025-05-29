---
title: ConditionalStyle.ParagraphFormat
linktitle: ParagraphFormat
articleTitle: ParagraphFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ParagraphFormat في ConditionalStyle لتتمكن من الوصول بسهولة إلى تنسيق الفقرات وإدارتها في أنماطك لتحسين عرض المستند.
type: docs
weight: 50
url: /ar/net/aspose.words/conditionalstyle/paragraphformat/
---
## ConditionalStyle.ParagraphFormat property

يحصل على تنسيق الفقرة للنمط الشرطي.

```csharp
public ParagraphFormat ParagraphFormat { get; }
```

## أمثلة

يوضح كيفية العمل مع أنماط مناطق معينة من الجدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Cell 3");
builder.InsertCell();
builder.Write("Cell 4");
builder.EndTable();

// إنشاء نمط جدول مخصص.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// الأنماط الشرطية هي تغييرات تنسيق تؤثر فقط على بعض خلايا الجدول
// بناءً على مسند، مثل وجود الخلايا في الصف الأخير.
// فيما يلي ثلاث طرق للوصول إلى أنماط الجدول الشرطية من مجموعة "ConditionalStyles".
// 1 - حسب نوع النمط:
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - حسب الفهرس:
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - كخاصية:
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// تطبيق الحشو وتنسيق النص على الأنماط الشرطية.
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// قم بإدراج جميع شروط الأسلوب الممكنة.
using (IEnumerator<ConditionalStyle> enumerator = tableStyle.ConditionalStyles.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        ConditionalStyle currentStyle = enumerator.Current;
        if (currentStyle != null) Console.WriteLine(currentStyle.Type);
    }
}

// قم بتطبيق النمط المخصص، الذي يحتوي على كافة الأنماط الشرطية، على الجدول.
table.Style = tableStyle;

//يطبق أسلوبنا بعض الأنماط الشرطية بشكل افتراضي.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// سوف نحتاج إلى تمكين جميع الأنماط الأخرى بأنفسنا عبر خاصية "StyleOptions".
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### أنظر أيضا

* class [ParagraphFormat](../../paragraphformat/)
* class [ConditionalStyle](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
