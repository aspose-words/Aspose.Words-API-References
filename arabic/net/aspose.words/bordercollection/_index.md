---
title: Class BorderCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.BorderCollection فصل. مجموعة منBorder الكائنات.
type: docs
weight: 90
url: /ar/net/aspose.words/bordercollection/
---
## BorderCollection class

مجموعة من[`Border`](../border/) الكائنات.

لمعرفة المزيد، قم بزيارة[البرمجة بالوثائق](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public sealed class BorderCollection : IEnumerable<Border>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Bottom](../../aspose.words/bordercollection/bottom/) { get; } | الحصول على الحد السفلي. |
| [Color](../../aspose.words/bordercollection/color/) { get; set; } | الحصول على لون الحدود أو تعيينه. |
| [Count](../../aspose.words/bordercollection/count/) { get; } | الحصول على عدد الحدود في المجموعة. |
| [DistanceFromText](../../aspose.words/bordercollection/distancefromtext/) { get; set; } | الحصول على أو تعيين مسافة الحد من النص بالنقاط. |
| [Horizontal](../../aspose.words/bordercollection/horizontal/) { get; } | يحصل على الحد الأفقي المستخدم بين الخلايا أو الفقرات المطابقة. |
| [Item](../../aspose.words/bordercollection/item/) { get; } | يسترد أ[`Border`](../border/) الكائن حسب نوع الحدود. (2 indexers) |
| [Left](../../aspose.words/bordercollection/left/) { get; } | يحصل على الحد الأيسر. |
| [LineStyle](../../aspose.words/bordercollection/linestyle/) { get; set; } | الحصول على نمط الحدود أو تعيينه. |
| [LineWidth](../../aspose.words/bordercollection/linewidth/) { get; set; } | الحصول على أو تعيين عرض الحدود بالنقاط. |
| [Right](../../aspose.words/bordercollection/right/) { get; } | يحصل على الحد الصحيح. |
| [Shadow](../../aspose.words/bordercollection/shadow/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان الحد يحتوي على ظل. |
| [Top](../../aspose.words/bordercollection/top/) { get; } | يحصل على الحد العلوي. |
| [Vertical](../../aspose.words/bordercollection/vertical/) { get; } | يحصل على الحد العمودي المستخدم بين الخلايا. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormatting](../../aspose.words/bordercollection/clearformatting/)() | إزالة كافة حدود الكائن. |
| [Equals](../../aspose.words/bordercollection/equals/#equals)(BorderCollection) | مقارنة مجموعات الحدود. |
| [GetEnumerator](../../aspose.words/bordercollection/getenumerator/)() | يُرجع كائن العداد الذي يمكن استخدامه للتكرار عبر كافة الحدود في المجموعة. |

### ملاحظات

عناصر المستند المختلفة لها حدود مختلفة. على سبيل المثال،[`ParagraphFormat`](../paragraphformat/)لديه[`Bottom`](./bottom/) ,[`Left`](./left/) ,[`Right`](./right/) و[`Top`](./top/) border. يمكنك تحديد تنسيق مختلف لكل حد بشكل مستقل أو تعداد كافة الحدود وتطبيق نفس التنسيق.

### أمثلة

يوضح كيفية إدراج فقرة ذات حد علوي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// قم بتعيين ThemeColor فقط عند ضبط LineWidth أو LineStyle.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### أنظر أيضا

* class [Border](../border/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


