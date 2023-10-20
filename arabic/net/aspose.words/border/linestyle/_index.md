---
title: Border.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words لـ .NET
description: Border LineStyle ملكية. الحصول على نمط الحدود أو تعيينه في C#.
type: docs
weight: 40
url: /ar/net/aspose.words/border/linestyle/
---
## Border.LineStyle property

الحصول على نمط الحدود أو تعيينه.

```csharp
public LineStyle LineStyle { get; set; }
```

## ملاحظات

إذا قمت بتعيين نمط الخط على لا شيء، فسيتم تغيير عرض الخط تلقائيًا إلى صفر.

## أمثلة

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

### أنظر أيضا

* enum [LineStyle](../../linestyle/)
* class [Border](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
