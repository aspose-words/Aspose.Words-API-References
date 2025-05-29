---
title: BorderCollection Class
linktitle: BorderCollection
articleTitle: BorderCollection
second_title: Aspose.Words لـ .NET
description: استكشف Aspose.Words.BorderCollection، الحل الأمثل لإدارة كائنات الحدود وتخصيصها بسهولة لتحسين تنسيق المستندات.
type: docs
weight: 280
url: /ar/net/aspose.words/bordercollection/
---
## BorderCollection class

مجموعة من[`Border`](../border/) الأشياء.

لمعرفة المزيد، قم بزيارة[البرمجة باستخدام المستندات](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public sealed class BorderCollection : IEnumerable<Border>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Bottom](../../aspose.words/bordercollection/bottom/) { get; } | يحصل على الحد السفلي. |
| [Color](../../aspose.words/bordercollection/color/) { get; set; } | يحصل على لون الحدود أو يعينه. |
| [Count](../../aspose.words/bordercollection/count/) { get; } | يحصل على عدد الحدود في المجموعة. |
| [DistanceFromText](../../aspose.words/bordercollection/distancefromtext/) { get; set; } | يحصل على أو يعين مسافة الحدود من النص بالنقاط. |
| [Horizontal](../../aspose.words/bordercollection/horizontal/) { get; } | يحصل على الحدود الأفقية المستخدمة بين الخلايا أو الفقرات المتوافقة. |
| [Item](../../aspose.words/bordercollection/item/) { get; } | يسترجع[`Border`](../border/) الكائن حسب نوع الحدود. (2 indexers) |
| [Left](../../aspose.words/bordercollection/left/) { get; } | يحصل على الحد الأيسر. |
| [LineStyle](../../aspose.words/bordercollection/linestyle/) { get; set; } | يحصل على نمط الحدود أو يعينه. |
| [LineWidth](../../aspose.words/bordercollection/linewidth/) { get; set; } | يحصل على عرض الحدود بالنقاط أو يعينه. |
| [Right](../../aspose.words/bordercollection/right/) { get; } | يحصل على الحد الصحيح. |
| [Shadow](../../aspose.words/bordercollection/shadow/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كانت الحدود تحتوي على ظل. |
| [Top](../../aspose.words/bordercollection/top/) { get; } | يحصل على الحد العلوي. |
| [Vertical](../../aspose.words/bordercollection/vertical/) { get; } | يحصل على الحدود الرأسية المستخدمة بين الخلايا. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormatting](../../aspose.words/bordercollection/clearformatting/)() | يزيل جميع حدود الكائن. |
| [Equals](../../aspose.words/bordercollection/equals/#equals)(*BorderCollection*) | يقارن مجموعات الحدود. |
| [GetEnumerator](../../aspose.words/bordercollection/getenumerator/)() | يعيد كائن عداد يمكن استخدامه للتكرار عبر جميع الحدود في المجموعة. |

## ملاحظات

تحتوي عناصر المستند المختلفة على حدود مختلفة. على سبيل المثال،[`ParagraphFormat`](../paragraphformat/) لديه[`Bottom`](./bottom/) ،[`Left`](./left/) ،[`Right`](./right/) و[`Top`](./top/) borders. يمكنك تحديد تنسيق مختلف لكل حدود بشكل مستقل أو حصر جميع الحدود وتطبيق نفس التنسيق.

## أمثلة

يوضح كيفية إدراج فقرة ذات حدود علوية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// قم بتعيين ThemeColor فقط عند تعيين LineWidth أو LineStyle.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### أنظر أيضا

* class [Border](../border/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
