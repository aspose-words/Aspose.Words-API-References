---
title: Class Border
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Border فصل. يمثل حدود الكائن.
type: docs
weight: 80
url: /ar/net/aspose.words/border/
---
## Border class

يمثل حدود الكائن.

لمعرفة المزيد، قم بزيارة[البرمجة بالوثائق](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public class Border : InternableComplexAttr
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Color](../../aspose.words/border/color/) { get; set; } | الحصول على لون الحدود أو تعيينه. |
| [DistanceFromText](../../aspose.words/border/distancefromtext/) { get; set; } | الحصول على أو تعيين مسافة الحد من النص أو من حافة الصفحة بالنقاط. |
| [IsVisible](../../aspose.words/border/isvisible/) { get; } | إرجاع`حقيقي` إذا[`LineStyle`](./linestyle/) ليسNone . |
| [LineStyle](../../aspose.words/border/linestyle/) { get; set; } | الحصول على نمط الحدود أو تعيينه. |
| [LineWidth](../../aspose.words/border/linewidth/) { get; set; } | الحصول على أو تعيين عرض الحدود بالنقاط. |
| [Shadow](../../aspose.words/border/shadow/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى ما إذا كان الحد يحتوي على ظل. |
| [ThemeColor](../../aspose.words/border/themecolor/) { get; set; } | الحصول على لون السمة أو تعيينه في نظام الألوان المطبق المرتبط بكائن الحدود هذا. |
| [TintAndShade](../../aspose.words/border/tintandshade/) { get; set; } | الحصول على أو تعيين قيمة مزدوجة تعمل على تفتيح اللون أو تغميقه. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormatting](../../aspose.words/border/clearformatting/)() | إعادة تعيين خصائص الحدود إلى القيم الافتراضية. |
| [Equals](../../aspose.words/border/equals/#equals)(Border) | تحديد ما إذا كان الحد المحدد مساويًا في القيمة للحد الحالي. |
| override [Equals](../../aspose.words/border/equals/#equals_1)(object) | تحديد ما إذا كان الكائن المحدد يساوي قيمة الكائن الحالي. |
| override [GetHashCode](../../aspose.words/border/gethashcode/)() | بمثابة دالة تجزئة لهذا النوع. |

### ملاحظات

يمكن تطبيق الحدود على عناصر الوثيقة المختلفة بما في ذلك الفقرة، ، تشغيل النص داخل فقرة أو خلية جدول.

### أمثلة

يوضح كيفية إدراج سلسلة محاطة بحد في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

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

* class [InternableComplexAttr](../internablecomplexattr/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


