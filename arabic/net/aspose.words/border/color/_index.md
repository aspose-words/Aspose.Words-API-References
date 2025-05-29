---
title: Border.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words لـ .NET
description: قم بتخصيص تصميماتك بسهولة باستخدام خاصية لون الحدود، التي تسمح لك بتعيين وتعديل ألوان الحدود للحصول على تأثير بصري مذهل.
type: docs
weight: 10
url: /ar/net/aspose.words/border/color/
---
## Border.Color property

يحصل على لون الحدود أو يعينه.

```csharp
public Color Color { get; set; }
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

* class [Border](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
