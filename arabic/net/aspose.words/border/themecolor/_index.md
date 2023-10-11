---
title: Border.ThemeColor
second_title: Aspose.Words لمراجع .NET API
description: Border ملكية. الحصول على لون السمة أو تعيينه في نظام الألوان المطبق المرتبط بكائن الحدود هذا.
type: docs
weight: 70
url: /ar/net/aspose.words/border/themecolor/
---
## Border.ThemeColor property

الحصول على لون السمة أو تعيينه في نظام الألوان المطبق المرتبط بكائن الحدود هذا.

```csharp
public ThemeColor ThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Border](../)
* مساحة الاسم [Aspose.Words](../../border/)
* المجسم [Aspose.Words](../../../)


