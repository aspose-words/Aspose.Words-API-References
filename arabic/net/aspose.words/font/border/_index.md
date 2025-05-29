---
title: Font.Border
linktitle: Border
articleTitle: Border
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية حدود الخط، التي توفر كائن حدود قابل للتخصيص لتعزيز نمط الخط ومرونة التصميم.
type: docs
weight: 60
url: /ar/net/aspose.words/font/border/
---
## Font.Border property

يعيد[`Border`](../../border/) الكائن الذي يحدد حدود الخط.

```csharp
public Border Border { get; }
```

## أمثلة

يوضح كيفية إدراج سلسلة محاطة بحدود في مستند.

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
