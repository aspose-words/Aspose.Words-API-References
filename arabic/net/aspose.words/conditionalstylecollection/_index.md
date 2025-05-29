---
title: ConditionalStyleCollection Class
linktitle: ConditionalStyleCollection
articleTitle: ConditionalStyleCollection
second_title: Aspose.Words لـ .NET
description: استكشف فئة Aspose.Words.ConditionalStyleCollection لإدارة كائنات ConditionalStyle بشكل فعال، وتحسين تنسيق المستندات وتخصيصها.
type: docs
weight: 520
url: /ar/net/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class

يمثل مجموعة من[`ConditionalStyle`](../conditionalstyle/) الأشياء.

لمعرفة المزيد، قم بزيارة[العمل مع الجداول](https://docs.aspose.com/words/net/working-with-tables/) مقالة توثيقية.

```csharp
public sealed class ConditionalStyleCollection : IEnumerable<ConditionalStyle>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BottomLeftCell](../../aspose.words/conditionalstylecollection/bottomleftcell/) { get; } | يحصل على نمط الخلية السفلية اليسرى. |
| [BottomRightCell](../../aspose.words/conditionalstylecollection/bottomrightcell/) { get; } | يحصل على نمط الخلية اليمنى السفلية. |
| [Count](../../aspose.words/conditionalstylecollection/count/) { get; } | يحصل على عدد الأنماط الشرطية في المجموعة. |
| [EvenColumnBanding](../../aspose.words/conditionalstylecollection/evencolumnbanding/) { get; } | يحصل على نمط شريط العمود الزوجي. |
| [EvenRowBanding](../../aspose.words/conditionalstylecollection/evenrowbanding/) { get; } | يحصل على نمط شريط الصف الزوجي. |
| [FirstColumn](../../aspose.words/conditionalstylecollection/firstcolumn/) { get; } | يحصل على نمط العمود الأول. |
| [FirstRow](../../aspose.words/conditionalstylecollection/firstrow/) { get; } | يحصل على نمط الصف الأول. |
| [Item](../../aspose.words/conditionalstylecollection/item/) { get; } | يسترجع[`ConditionalStyle`](../conditionalstyle/) الكائن حسب نوع النمط الشرطي. (2 indexers) |
| [LastColumn](../../aspose.words/conditionalstylecollection/lastcolumn/) { get; } | يحصل على نمط العمود الأخير. |
| [LastRow](../../aspose.words/conditionalstylecollection/lastrow/) { get; } | يحصل على نمط الصف الأخير. |
| [OddColumnBanding](../../aspose.words/conditionalstylecollection/oddcolumnbanding/) { get; } | يحصل على نمط شريط العمود الغريب. |
| [OddRowBanding](../../aspose.words/conditionalstylecollection/oddrowbanding/) { get; } | يحصل على نمط شريط الصف الغريب. |
| [TopLeftCell](../../aspose.words/conditionalstylecollection/topleftcell/) { get; } | يحصل على نمط الخلية العلوية اليسرى. |
| [TopRightCell](../../aspose.words/conditionalstylecollection/toprightcell/) { get; } | يحصل على نمط الخلية اليمنى العلوية. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstylecollection/clearformatting/)() | مسح جميع الأنماط الشرطية لنمط الجدول. |
| [GetEnumerator](../../aspose.words/conditionalstylecollection/getenumerator/)() | يعيد كائن عداد يمكن استخدامه للتكرار على جميع الأنماط الشرطية في المجموعة. |

## ملاحظات

لا يُمكن إضافة أو إزالة عناصر من هذه المجموعة. تحتوي على مجموعة دائمة من العناصر: عنصر واحد لكل قيمة من قيم x000d.[`ConditionalStyleType`](../conditionalstyletype/) نوع التعداد.

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

* class [ConditionalStyle](../conditionalstyle/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
