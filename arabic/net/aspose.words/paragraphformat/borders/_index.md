---
title: ParagraphFormat.Borders
second_title: Aspose.Words لمراجع .NET API
description: ParagraphFormat ملكية. الحصول على مجموعة من حدود الفقرة .
type: docs
weight: 50
url: /ar/net/aspose.words/paragraphformat/borders/
---
## ParagraphFormat.Borders property

الحصول على مجموعة من حدود الفقرة .

```csharp
public BorderCollection Borders { get; }
```

### أمثلة

يوضح كيفية إدراج فقرة بحد علوي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders[BorderType.Top];
topBorder.Color = Color.Red;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;

builder.Writeln("Text with a red top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### أنظر أيضا

* class [BorderCollection](../../bordercollection/)
* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../paragraphformat/)
* المجسم [Aspose.Words](../../../)


