---
title: Font.Border
linktitle: Border
articleTitle: Border
second_title: Aspose.Words لـ .NET
description: Font Border ملكية. إرجاع أBorder الكائن الذي يحدد الحدود للخط في C#.
type: docs
weight: 60
url: /ar/net/aspose.words/font/border/
---
## Font.Border property

إرجاع أ[`Border`](../../border/) الكائن الذي يحدد الحدود للخط.

```csharp
public Border Border { get; }
```

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

* class [Border](../../border/)
* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
