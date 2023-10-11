---
title: ParagraphFormat.Borders
second_title: Aspose.Words لمراجع .NET API
description: ParagraphFormat ملكية. الحصول على مجموعة حدود الفقرة.
type: docs
weight: 60
url: /ar/net/aspose.words/paragraphformat/borders/
---
## ParagraphFormat.Borders property

الحصول على مجموعة حدود الفقرة.

```csharp
public BorderCollection Borders { get; }
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

* class [BorderCollection](../../bordercollection/)
* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../paragraphformat/)
* المجسم [Aspose.Words](../../../)


