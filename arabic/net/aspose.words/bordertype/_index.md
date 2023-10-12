---
title: Enum BorderType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.BorderType تعداد. يحدد جوانب الحدود.
type: docs
weight: 100
url: /ar/net/aspose.words/bordertype/
---
## BorderType enumeration

يحدد جوانب الحدود.

لمعرفة المزيد، قم بزيارة[البرمجة بالوثائق](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public enum BorderType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `-1` | القيمة الافتراضية. |
| Bottom | `0` | تحديد الحد السفلي لفقرة أو خلية جدول. |
| Left | `1` | تحديد الحد الأيسر لفقرة أو خلية جدول. |
| Right | `2` | تحديد الحد الأيمن لفقرة أو خلية جدول. |
| Top | `3` | يحدد الحد العلوي لفقرة أو خلية جدول. |
| Horizontal | `4` | يحدد الحدود الأفقية بين الخلايا في الجدول أو بين الفقرات المطابقة. |
| Vertical | `5` | تحديد الحدود العمودية بين الخلايا في الجدول. |
| DiagonalDown | `6` | تحديد الحد القطري في خلية الجدول. |
| DiagonalUp | `7` | تحديد الحد القطري في خلية الجدول. |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


