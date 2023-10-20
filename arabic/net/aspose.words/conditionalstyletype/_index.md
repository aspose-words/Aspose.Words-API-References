---
title: ConditionalStyleType Enum
linktitle: ConditionalStyleType
articleTitle: ConditionalStyleType
second_title: Aspose.Words لـ .NET
description: Aspose.Words.ConditionalStyleType تعداد. يمثل مناطق الجدول المحتملة التي يمكن تعريف التنسيق الشرطي لها في نمط الجدول في C#.
type: docs
weight: 330
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
| FirstRow | `0` | تحديد تنسيق الصف الأول من الجدول. |
| FirstColumn | `1` | تحديد تنسيق العمود الأول من الجدول. |
| LastRow | `2` | تحديد تنسيق الصف الأخير من الجدول. |
| LastColumn | `3` | تحديد تنسيق العمود الأخير في الجدول. |
| OddRowBanding | `4` | تحديد تنسيق شريط الصفوف ذات الأرقام الفردية. |
| OddColumnBanding | `5` | تحديد تنسيق شريط الأعمدة ذات الأرقام الفردية. |
| EvenRowBanding | `6` | يحدد تنسيق شريط الصف ذو الأرقام الزوجية. |
| EvenColumnBanding | `7` | تحديد تنسيق شريط الأعمدة ذات الأرقام الزوجية. |
| TopLeftCell | `8` | تحديد تنسيق الخلية العلوية اليسرى للجدول. |
| TopRightCell | `9` | تحديد تنسيق الخلية العلوية اليمنى للجدول. |
| BottomLeftCell | `10` | تحديد تنسيق الخلية اليسرى السفلية للجدول. |
| BottomRightCell | `11` | تحديد تنسيق الخلية اليمنى السفلية للجدول. |

## أمثلة

يوضح كيفية العمل مع أنماط مناطق معينة في الجدول.

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

// الأنماط الشرطية هي تغييرات التنسيق التي تؤثر فقط على بعض خلايا الجدول
// استنادًا إلى المسند، مثل وجود الخلايا في الصف الأخير.
// فيما يلي ثلاث طرق للوصول إلى الأنماط الشرطية لنمط الجدول من مجموعة "الأنماط الشرطية".
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

// قم بإدراج جميع شروط النمط الممكنة.
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

// يطبق أسلوبنا بعض الأنماط الشرطية بشكل افتراضي.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// سنحتاج إلى تمكين جميع الأنماط الأخرى بأنفسنا عبر خاصية "StyleOptions".
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
