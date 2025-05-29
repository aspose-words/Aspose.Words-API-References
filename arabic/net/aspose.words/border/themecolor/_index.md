---
title: Border.ThemeColor
linktitle: ThemeColor
articleTitle: ThemeColor
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام خاصية Border ThemeColor لتخصيص مخطط الألوان الخاص بك وتعزيز تصميمك باستخدام سمات نابضة بالحياة ومصممة خصيصًا.
type: docs
weight: 70
url: /ar/net/aspose.words/border/themecolor/
---
## Border.ThemeColor property

يحصل على لون السمة أو يعينه في مخطط الألوان المطبق المرتبط بكائن الحدود هذا.

```csharp
public ThemeColor ThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Border](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
