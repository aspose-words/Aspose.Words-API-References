---
title: Font.Emboss
linktitle: Emboss
articleTitle: Emboss
second_title: Aspose.Words لـ .NET
description: Font Emboss ملكية. صحيح إذا كان الخط منسقًا بشكل منقوش في C#.
type: docs
weight: 100
url: /ar/net/aspose.words/font/emboss/
---
## Font.Emboss property

صحيح إذا كان الخط منسقًا بشكل منقوش.

```csharp
public bool Emboss { get; set; }
```

## أمثلة

يوضح كيفية تطبيق تأثيرات النقش/النقش على النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// فيما يلي طريقتان لاستخدام الظلال لتطبيق تأثير ثلاثي الأبعاد على النص.
// 1 - نقش النص ليبدو وكأن الحروف غائرة في الصفحة:
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 - نقش النص ليبدو وكأن الحروف تخرج من الصفحة:
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
