---
title: Border.Color
second_title: Aspose.Words لمراجع .NET API
description: Border ملكية. الحصول على لون الحدود أو تعيينه.
type: docs
weight: 10
url: /ar/net/aspose.words/border/color/
---
## Border.Color property

الحصول على لون الحدود أو تعيينه.

```csharp
public Color Color { get; set; }
```

### أمثلة

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

* class [Border](../)
* مساحة الاسم [Aspose.Words](../../border/)
* المجسم [Aspose.Words](../../../)


