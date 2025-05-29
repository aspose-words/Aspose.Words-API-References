---
title: ConditionalStyle Class
linktitle: ConditionalStyle
articleTitle: ConditionalStyle
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.ConditionalStyle لتنسيق الجداول المتقدم. حسّن مستنداتك بأنماط ديناميكية وحسّن قابلية القراءة بسهولة.
type: docs
weight: 510
url: /ar/net/aspose.words/conditionalstyle/
---
## ConditionalStyle class

يمثل تنسيقًا خاصًا يتم تطبيقه على بعض مناطق الجدول باستخدام نمط الجدول المخصص.

لمعرفة المزيد، قم بزيارة[العمل مع الجداول](https://docs.aspose.com/words/net/working-with-tables/) مقالة توثيقية.

```csharp
public sealed class ConditionalStyle
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Borders](../../aspose.words/conditionalstyle/borders/) { get; } | يحصل على مجموعة حدود الخلايا الافتراضية للنمط الشرطي. |
| [BottomPadding](../../aspose.words/conditionalstyle/bottompadding/) { get; set; } | يحصل على مقدار المساحة (بالنقاط) المراد إضافتها أسفل محتويات خلايا الجدول أو يعينه. |
| [Font](../../aspose.words/conditionalstyle/font/) { get; } | يحصل على تنسيق الأحرف للنمط الشرطي. |
| [LeftPadding](../../aspose.words/conditionalstyle/leftpadding/) { get; set; } | يحصل على مقدار المساحة (بالنقاط) التي يجب إضافتها إلى يسار محتويات خلايا الجدول أو يعينها. |
| [ParagraphFormat](../../aspose.words/conditionalstyle/paragraphformat/) { get; } | يحصل على تنسيق الفقرة للنمط الشرطي. |
| [RightPadding](../../aspose.words/conditionalstyle/rightpadding/) { get; set; } | يحصل على مقدار المساحة (بالنقاط) التي يجب إضافتها إلى يمين محتويات خلايا الجدول أو يعينها. |
| [Shading](../../aspose.words/conditionalstyle/shading/) { get; } | يحصل على[`Shading`](../shading/) الكائن الذي يشير إلى تنسيق التظليل لهذا النمط الشرطي. |
| [TopPadding](../../aspose.words/conditionalstyle/toppadding/) { get; set; } | يحصل على مقدار المساحة (بالنقاط) المراد إضافتها فوق محتويات خلايا الجدول أو يعينه. |
| [Type](../../aspose.words/conditionalstyle/type/) { get; } | يحصل على منطقة الجدول التي يرتبط بها هذا النمط الشرطي. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstyle/clearformatting/)() | مسح تنسيق هذا النمط الشرطي. |
| override [Equals](../../aspose.words/conditionalstyle/equals/)(*object*) | يقارن هذا النمط الشرطي بالكائن المحدد. |
| override [GetHashCode](../../aspose.words/conditionalstyle/gethashcode/)() | يحسب رمز التجزئة لهذا الكائن. |

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
