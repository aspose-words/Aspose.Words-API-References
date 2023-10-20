---
title: TableStyle Class
linktitle: TableStyle
articleTitle: TableStyle
second_title: Aspose.Words لـ .NET
description: Aspose.Words.TableStyle فصل. يمثل نمط الجدول في C#.
type: docs
weight: 6220
url: /ar/net/aspose.words/tablestyle/
---
## TableStyle class

يمثل نمط الجدول.

لمعرفة المزيد، قم بزيارة[العمل مع الجداول](https://docs.aspose.com/words/net/working-with-tables/) مقالة توثيقية.

```csharp
public class TableStyle : Style
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | يحصل على كافة الأسماء المستعارة لهذا النمط. إذا لم يكن النمط يحتوي على أسماء مستعارة، فسيتم إرجاع مجموعة فارغة من السلسلة. |
| [Alignment](../../aspose.words/tablestyle/alignment/) { get; set; } | يحدد المحاذاة لنمط الجدول. |
| [AllowBreakAcrossPages](../../aspose.words/tablestyle/allowbreakacrosspages/) { get; set; } | الحصول على أو تعيين علامة تشير إلى ما إذا كان النص الموجود في صف الجدول مسموحًا بتقسيمه عبر فاصل الصفحات. |
| [AutomaticallyUpdate](../../aspose.words/style/automaticallyupdate/) { get; set; } | يحدد ما إذا كان سيتم إعادة تعريف هذا النمط تلقائيًا بناءً على القيمة المناسبة. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | الحصول على/تعيين اسم النمط الذي يعتمد عليه هذا النمط. |
| [Bidi](../../aspose.words/tablestyle/bidi/) { get; set; } | الحصول على أو تعيين ما إذا كان هذا هو النمط لجدول من اليمين إلى اليسار. |
| [Borders](../../aspose.words/tablestyle/borders/) { get; } | الحصول على مجموعة حدود الخلايا الافتراضية للنمط. |
| [BottomPadding](../../aspose.words/tablestyle/bottompadding/) { get; set; } | الحصول على أو تعيين مقدار المسافة (بالنقاط) لإضافتها أسفل محتويات خلايا الجدول. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | صحيح إذا كان هذا النمط أحد الأنماط المضمنة في برنامج MS Word. |
| [CellSpacing](../../aspose.words/tablestyle/cellspacing/) { get; set; } | الحصول على أو تعيين مقدار المسافة (بالنقاط) بين الخلايا. |
| [ColumnStripe](../../aspose.words/tablestyle/columnstripe/) { get; set; } | الحصول على أو تعيين عدد من الأعمدة لتضمينها في النطاق عندما يحدد النمط نطاق الأعمدة الفردية/الزوجية. |
| [ConditionalStyles](../../aspose.words/tablestyle/conditionalstyles/) { get; } | مجموعة من الأنماط الشرطية التي يمكن تعريفها لنمط الجدول هذا. |
| [Document](../../aspose.words/style/document/) { get; } | الحصول على مستند المالك. |
| [Font](../../aspose.words/style/font/) { get; } | الحصول على تنسيق الأحرف للنمط. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | صحيح عندما يكون النمط أحد أنماط العناوين المضمنة. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | يحدد ما إذا كان سيتم عرض هذا النمط في معرض "الأنماط السريعة" داخل واجهة مستخدم MS Word. |
| [LeftIndent](../../aspose.words/tablestyle/leftindent/) { get; set; } | الحصول على أو تعيين القيمة التي تمثل المسافة البادئة اليسرى للجدول. |
| [LeftPadding](../../aspose.words/tablestyle/leftpadding/) { get; set; } | الحصول على أو تعيين مقدار المسافة (بالنقاط) المراد إضافتها إلى يسار محتويات خلايا الجدول. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; } | يحصل على اسم[`Style`](../style/) مرتبطة بهذا. إرجاع سلسلة فارغة إذا لم يتم ربط أي أنماط. |
| [List](../../aspose.words/style/list/) { get; } | الحصول على القائمة التي تحدد تنسيق نمط القائمة هذا. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | يوفر الوصول إلى خصائص تنسيق القائمة لنمط الفقرة. |
| [Name](../../aspose.words/style/name/) { get; set; } | الحصول على اسم النمط أو تعيينه. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | الحصول على/تعيين اسم النمط الذي سيتم تطبيقه تلقائيًا على فقرة جديدة تم إدراجها بعد a فقرة منسقة بالنمط المحدد. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | الحصول على تنسيق الفقرة للنمط. |
| [RightPadding](../../aspose.words/tablestyle/rightpadding/) { get; set; } | الحصول على أو تعيين مقدار المسافة (بالنقاط) المراد إضافتها إلى يمين محتويات خلايا الجدول. |
| [RowStripe](../../aspose.words/tablestyle/rowstripe/) { get; set; } | الحصول على أو تعيين عدد من الصفوف لتضمينها في النطاق عندما يحدد النمط نطاق الصفوف الفردية/الزوجية. |
| [Shading](../../aspose.words/tablestyle/shading/) { get; } | يحصل على[`Shading`](../shading/) الكائن الذي يشير إلى تنسيق التظليل لخلايا الجدول. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | الحصول على معرف النمط المحلي المستقل للنمط المدمج. |
| [Styles](../../aspose.words/style/styles/) { get; } | الحصول على مجموعة الأنماط التي ينتمي إليها هذا النمط. |
| [TopPadding](../../aspose.words/tablestyle/toppadding/) { get; set; } | الحصول على أو تعيين مقدار المسافة (بالنقاط) لإضافتها فوق محتويات خلايا الجدول. |
| [Type](../../aspose.words/style/type/) { get; } | الحصول على نوع النمط (فقرة أو حرف). |
| [VerticalAlignment](../../aspose.words/tablestyle/verticalalignment/) { get; set; } | يحدد المحاذاة العمودية للخلايا. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Equals](../../aspose.words/style/equals/)(*[Style](../style/)*) | يقارن مع النمط المحدد. تتم مقارنة أنماط الأنماط للأنماط المضمنة فقط. لا يتم تضمين افتراضيات الأنماط في المقارنة. تتم مقارنة النمط الأساسي والنمط المرتبط ونمط الفقرة التالية بشكل متكرر. |
| [Remove](../../aspose.words/style/remove/)() | إزالة النمط المحدد من المستند. |

## أمثلة

يوضح كيفية إنشاء إعدادات نمط مخصصة للجدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// قد يؤثر تعيين خصائص نمط الجدول على خصائص الجدول نفسه.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### أنظر أيضا

* class [Style](../style/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
