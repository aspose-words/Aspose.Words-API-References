---
title: Border Class
linktitle: Border
articleTitle: Border
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Border، الحل الأمثل لتخصيص حدود الكائنات في المستندات. حسّن مشاريعك بدقة وأناقة!
type: docs
weight: 270
url: /ar/net/aspose.words/border/
---
## Border class

يمثل حدود الكائن.

لمعرفة المزيد، قم بزيارة[البرمجة باستخدام المستندات](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public class Border : InternableComplexAttr
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Color](../../aspose.words/border/color/) { get; set; } | يحصل على لون الحدود أو يعينه. |
| [DistanceFromText](../../aspose.words/border/distancefromtext/) { get; set; } | يحصل على أو يعين مسافة الحدود من النص أو من حافة الصفحة بالنقاط. |
| [IsVisible](../../aspose.words/border/isvisible/) { get; } | إرجاع`حقيقي` إذا كان[`LineStyle`](./linestyle/) ليس كذلكNone . |
| [LineStyle](../../aspose.words/border/linestyle/) { get; set; } | يحصل على نمط الحدود أو يعينه. |
| [LineWidth](../../aspose.words/border/linewidth/) { get; set; } | يحصل على عرض الحدود بالنقاط أو يعينه. |
| [Shadow](../../aspose.words/border/shadow/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كانت الحدود تحتوي على ظل. |
| [ThemeColor](../../aspose.words/border/themecolor/) { get; set; } | يحصل على لون السمة أو يعينه في مخطط الألوان المطبق المرتبط بكائن الحدود هذا. |
| [TintAndShade](../../aspose.words/border/tintandshade/) { get; set; } | يحصل على قيمة مزدوجة لتفتيح اللون أو تعتيمه أو تعيينها. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormatting](../../aspose.words/border/clearformatting/)() | إعادة تعيين خصائص الحدود إلى القيم الافتراضية. |
| [Equals](../../aspose.words/border/equals/#equals)(*Border*) | يحدد ما إذا كانت الحدود المحددة مساوية في القيمة للحد الحالي. |
| override [Equals](../../aspose.words/border/equals/#equals_1)(*object*) | يحدد ما إذا كان الكائن المحدد يساوي في القيمة الكائن الحالي. |
| override [GetHashCode](../../aspose.words/border/gethashcode/)() | يعمل كدالة تجزئة لهذا النوع. |

## ملاحظات

يمكن تطبيق الحدود على عناصر مختلفة في المستند بما في ذلك الفقرة أو سلسلة من النص داخل فقرة أو خلية جدول.

## أمثلة

يوضح كيفية إدراج سلسلة محاطة بحدود في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

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

* class [InternableComplexAttr](../internablecomplexattr/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
