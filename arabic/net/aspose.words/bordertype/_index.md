---
title: BorderType Enum
linktitle: BorderType
articleTitle: BorderType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.BorderType enum لخيارات حدود قابلة للتخصيص. حسّن مستنداتك بتحكم دقيق في الحدود وأسلوبها!
type: docs
weight: 290
url: /ar/net/aspose.words/bordertype/
---
## BorderType enumeration

يحدد جوانب الحدود.

لمعرفة المزيد، قم بزيارة[البرمجة باستخدام المستندات](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public enum BorderType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `-1` | القيمة الافتراضية. |
| Bottom | `0` | يحدد الحد السفلي للفقرة أو خلية الجدول. |
| Left | `1` | يحدد الحد الأيسر للفقرة أو خلية الجدول. |
| Right | `2` | يحدد الحد الأيمن للفقرة أو خلية الجدول. |
| Top | `3` | يحدد الحد العلوي للفقرة أو خلية الجدول. |
| Horizontal | `4` | يحدد الحدود الأفقية بين الخلايا في جدول أو بين الفقرات المتطابقة. |
| Vertical | `5` | يحدد الحدود الرأسية بين الخلايا في الجدول. |
| DiagonalDown | `6` | يحدد الحدود القطرية في خلية الجدول. |
| DiagonalUp | `7` | يحدد الحدود القطرية في خلية الجدول. |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
