---
title: Border.TintAndShade
second_title: Aspose.Words لمراجع .NET API
description: Border ملكية. الحصول على أو تعيين قيمة مزدوجة تعمل على تفتيح اللون أو تغميقه.
type: docs
weight: 80
url: /ar/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

الحصول على أو تعيين قيمة مزدوجة تعمل على تفتيح اللون أو تغميقه.

```csharp
public double TintAndShade { get; set; }
```

### ملاحظات

تتراوح القيم المسموح بها من -1 (الأغمق) إلى 1 (الأفتح) لهذه الخاصية. الصفر (0) محايد. محاولة تعيين هذه الخاصية إلى قيمة أقل من -1 أو أكثر من 1 تؤدي إلىArgumentOutOfRangeException.

يؤدي تعيين هذه الخاصية للكائن الحدودي الذي يحتوي على ألوان غير موضوعية إلى حدوث ذلكInvalidOperationException.

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

* class [Border](../)
* مساحة الاسم [Aspose.Words](../../border/)
* المجسم [Aspose.Words](../../../)


