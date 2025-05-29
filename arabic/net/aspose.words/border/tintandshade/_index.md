---
title: Border.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words لـ .NET
description: اكتشف Border TintAndShade، واضبط سطوع الألوان بسهولة باستخدام قيمة مضاعفة بسيطة لتحسينات تصميمية مذهلة. مثالي لمشاريعك الإبداعية!
type: docs
weight: 80
url: /ar/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

يحصل على قيمة مزدوجة لتفتيح اللون أو تعتيمه أو تعيينها.

```csharp
public double TintAndShade { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | يتم رميها إذا حاولت تعيين هذه الخاصية إلى قيمة أقل من -1 أو أكثر من 1. |
| InvalidOperationException | يتم الرمي إذا تم تعيين هذه الخاصية لكائن الحدود بألوان غير خاصة بالموضوع. |

## ملاحظات

القيم المسموح بها تتراوح من -1 (الأغمق) إلى 1 (الأفتح) لهذه الخاصية. الصفر (0) محايد.

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

* class [Border](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
