---
title: ConditionalStyleCollection
second_title: Aspose.Words لمراجع .NET API
description: يمثل مجموعة منConditionalStyle./conditionalstyle الكائنات ._ x000d_
type: docs
weight: 310
url: /ar/net/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class

يمثل مجموعة من[`ConditionalStyle`](../conditionalstyle) الكائنات ._ x000d_

```csharp
public sealed class ConditionalStyleCollection : IEnumerable<ConditionalStyle>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BottomLeftCell](../../aspose.words/conditionalstylecollection/bottomleftcell) { get; } | الحصول على نمط الخلية اليسرى السفلية. |
| [BottomRightCell](../../aspose.words/conditionalstylecollection/bottomrightcell) { get; } | الحصول على نمط الخلية الأيمن السفلي. |
| [Count](../../aspose.words/conditionalstylecollection/count) { get; } | الحصول على عدد الأنماط الشرطية في المجموعة. |
| [EvenColumnBanding](../../aspose.words/conditionalstylecollection/evencolumnbanding) { get; } | الحصول على نمط نطاقات الأعمدة الزوجية ._ x000d_ |
| [EvenRowBanding](../../aspose.words/conditionalstylecollection/evenrowbanding) { get; } | يحصل على نمط نطاقات الصف الزوجي . |
| [FirstColumn](../../aspose.words/conditionalstylecollection/firstcolumn) { get; } | يحصل على نمط العمود الأول ._ x000d_ |
| [FirstRow](../../aspose.words/conditionalstylecollection/firstrow) { get; } | يحصل على نمط الصف الأول ._ x000d_ |
| [Item](../../aspose.words/conditionalstylecollection/item) { get; } | يسترجع أ[`ConditionalStyle`](../conditionalstyle) الكائن حسب نوع النمط الشرطي. (2 indexers) |
| [LastColumn](../../aspose.words/conditionalstylecollection/lastcolumn) { get; } | الحصول على نمط العمود الأخير ._ x000d_ |
| [LastRow](../../aspose.words/conditionalstylecollection/lastrow) { get; } | يحصل على نمط الصف الأخير ._ x000d_ |
| [OddColumnBanding](../../aspose.words/conditionalstylecollection/oddcolumnbanding) { get; } | يحصل على نمط نطاقات العمود الفردي ._ x000d_ |
| [OddRowBanding](../../aspose.words/conditionalstylecollection/oddrowbanding) { get; } | يحصل على نمط نطاقات الصف الفردي ._ x000d_ |
| [TopLeftCell](../../aspose.words/conditionalstylecollection/topleftcell) { get; } | الحصول على نمط الخلية الأيسر العلوي ._ x000d_ |
| [TopRightCell](../../aspose.words/conditionalstylecollection/toprightcell) { get; } | الحصول على نمط الخلية الأيمن العلوي ._ x000d_ |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstylecollection/clearformatting)() | يمسح كل الأنماط الشرطية لنمط الجدول. |
| [GetEnumerator](../../aspose.words/conditionalstylecollection/getenumerator)() | إرجاع كائن العداد الذي يمكن استخدامه للتكرار على كافة الأنماط الشرطية في المجموعة. |

### ملاحظات

لا يمكن إضافة أو إزالة عناصر من هذه المجموعة. يحتوي على مجموعة دائمة من العناصر: عنصر واحد مقابل_ x000d_ لكل قيمة من[`ConditionalStyleType`](../conditionalstyletype) نوع التعداد ._ x000d_

### أمثلة

يوضح كيفية التعامل مع أنماط منطقة معينة في الجدول.

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
// استنادًا إلى المسند ، مثل وجود الخلايا في الصف الأخير.
// فيما يلي ثلاث طرق للوصول إلى الأنماط الشرطية لنمط الجدول من مجموعة "ConditionalStyles".
// 1 - حسب نوع النمط:
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - حسب الفهرس:
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - كممتلكات:
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// تطبيق تنسيق النص والحشو على الأنماط الشرطية.
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// قائمة بجميع شروط النمط الممكنة.
using (IEnumerator<ConditionalStyle> enumerator = tableStyle.ConditionalStyles.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        ConditionalStyle currentStyle = enumerator.Current;
        if (currentStyle != null) Console.WriteLine(currentStyle.Type);
    }
}

// قم بتطبيق النمط المخصص ، الذي يحتوي على جميع الأنماط الشرطية ، على الجدول.
table.Style = tableStyle;

// يطبق أسلوبنا بعض الأنماط الشرطية افتراضيًا.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// سنحتاج إلى تمكين جميع الأنماط الأخرى بأنفسنا عبر خاصية "StyleOptions".
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### أنظر أيضا

* class [ConditionalStyle](../conditionalstyle)
* مساحة الاسم [Aspose.Words](../../aspose.words)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
