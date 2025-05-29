---
title: ParagraphFormat.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ParagraphFormat Borders لإدارة حدود فقراتك وتخصيصها بسهولة، مما يعزز جماليات المستند وسهولة قراءته.
type: docs
weight: 60
url: /ar/net/aspose.words/paragraphformat/borders/
---
## ParagraphFormat.Borders property

يحصل على مجموعة من حدود الفقرة.

```csharp
public BorderCollection Borders { get; }
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

* class [BorderCollection](../../bordercollection/)
* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
