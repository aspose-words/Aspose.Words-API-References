---
title: ConditionalStyleType Enum
linktitle: ConditionalStyleType
articleTitle: ConditionalStyleType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.ConditionalStyleType enum لتحديد تنسيق الجداول الديناميكي. حسّن أنماط مستنداتك بخيارات مرنة وشرطية!
type: docs
weight: 530
url: /ar/net/aspose.words/conditionalstyletype/
---
## ConditionalStyleType enumeration

يمثل مناطق الجدول المحتملة التي يمكن تعريف التنسيق الشرطي لها في نمط الجدول.

```csharp
public enum ConditionalStyleType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| FirstRow | `0` | يحدد تنسيق الصف الأول من الجدول. |
| FirstColumn | `1` | يحدد تنسيق العمود الأول من الجدول. |
| LastRow | `2` | يحدد تنسيق الصف الأخير من الجدول. |
| LastColumn | `3` | يحدد تنسيق العمود الأخير في الجدول. |
| OddRowBanding | `4` | يحدد تنسيق شريط الصفوف ذي الأرقام الفردية. |
| OddColumnBanding | `5` | يحدد تنسيق شريط الأعمدة ذي الأرقام الفردية. |
| EvenRowBanding | `6` | يحدد تنسيق شريط الصفوف الزوجية. |
| EvenColumnBanding | `7` | يحدد تنسيق شريط الأعمدة الزوجي. |
| TopLeftCell | `8` | يحدد تنسيق الخلية العلوية اليسرى من الجدول. |
| TopRightCell | `9` | يحدد تنسيق الخلية اليمنى العلوية للجدول. |
| BottomLeftCell | `10` | يحدد تنسيق الخلية اليسرى السفلية للجدول. |
| BottomRightCell | `11` | يحدد تنسيق الخلية اليمنى السفلية للجدول. |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
