---
title: Border.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words لـ .NET
description: قم بضبط خاصية Border LineWidth لتخصيص سمك الحدود بالنقاط، مما يعزز دقة تصميمك وجاذبيته البصرية.
type: docs
weight: 50
url: /ar/net/aspose.words/border/linewidth/
---
## Border.LineWidth property

يحصل على عرض الحدود بالنقاط أو يعينه.

```csharp
public double LineWidth { get; set; }
```

## ملاحظات

إذا قمت بتعيين عرض الخط أكبر من الصفر عندما يكون نمط الخط لا شيء، فسيتم تغيير نمط الخط is تلقائيًا إلى خط واحد.

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

* class [Border](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
