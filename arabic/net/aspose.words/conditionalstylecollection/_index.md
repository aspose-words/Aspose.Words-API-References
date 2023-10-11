---
title: Class ConditionalStyleCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.ConditionalStyleCollection فصل. يمثل مجموعة منConditionalStyle الكائنات.
type: docs
weight: 320
url: /ar/net/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class

يمثل مجموعة من[`ConditionalStyle`](../conditionalstyle/) الكائنات.

لمعرفة المزيد، قم بزيارة[العمل مع الجداول](https://docs.aspose.com/words/net/working-with-tables/) مقالة توثيقية.

```csharp
public sealed class ConditionalStyleCollection : IEnumerable<ConditionalStyle>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BottomLeftCell](../../aspose.words/conditionalstylecollection/bottomleftcell/) { get; } | الحصول على نمط الخلية اليسرى السفلية. |
| [BottomRightCell](../../aspose.words/conditionalstylecollection/bottomrightcell/) { get; } | الحصول على نمط الخلية اليمنى السفلية. |
| [Count](../../aspose.words/conditionalstylecollection/count/) { get; } | الحصول على عدد الأنماط الشرطية في المجموعة. |
| [EvenColumnBanding](../../aspose.words/conditionalstylecollection/evencolumnbanding/) { get; } | الحصول على نمط ربط الأعمدة الزوجية. |
| [EvenRowBanding](../../aspose.words/conditionalstylecollection/evenrowbanding/) { get; } | الحصول على نمط ربط الصفوف الزوجية. |
| [FirstColumn](../../aspose.words/conditionalstylecollection/firstcolumn/) { get; } | الحصول على نمط العمود الأول. |
| [FirstRow](../../aspose.words/conditionalstylecollection/firstrow/) { get; } | الحصول على نمط الصف الأول. |
| [Item](../../aspose.words/conditionalstylecollection/item/) { get; } | يسترد أ[`ConditionalStyle`](../conditionalstyle/) كائن حسب نوع النمط الشرطي. (2 indexers) |
| [LastColumn](../../aspose.words/conditionalstylecollection/lastcolumn/) { get; } | الحصول على نمط العمود الأخير. |
| [LastRow](../../aspose.words/conditionalstylecollection/lastrow/) { get; } | الحصول على نمط الصف الأخير. |
| [OddColumnBanding](../../aspose.words/conditionalstylecollection/oddcolumnbanding/) { get; } | الحصول على نمط نطاق الأعمدة الفردي. |
| [OddRowBanding](../../aspose.words/conditionalstylecollection/oddrowbanding/) { get; } | الحصول على نمط نطاقات الصفوف الفردية. |
| [TopLeftCell](../../aspose.words/conditionalstylecollection/topleftcell/) { get; } | الحصول على نمط الخلية العلوية اليسرى. |
| [TopRightCell](../../aspose.words/conditionalstylecollection/toprightcell/) { get; } | الحصول على نمط الخلية العلوي الأيمن. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstylecollection/clearformatting/)() | مسح كافة الأنماط الشرطية لنمط الجدول. |
| [GetEnumerator](../../aspose.words/conditionalstylecollection/getenumerator/)() | يُرجع كائن العداد الذي يمكن استخدامه للتكرار على جميع الأنماط الشرطية في المجموعة. |

### ملاحظات

لا يمكن إضافة أو إزالة عناصر من هذه المجموعة. يحتوي على مجموعة دائمة من العناصر: عنصر واحد for لكل قيمة[`ConditionalStyleType`](../conditionalstyletype/) نوع التعداد.

### أمثلة

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

* class [ConditionalStyle](../conditionalstyle/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


