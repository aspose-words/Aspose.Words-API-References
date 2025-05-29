---
title: Font.Emboss
linktitle: Emboss
articleTitle: Emboss
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Font Emboss، التي تُحسّن نصك بتأثير نقش أنيق لتصاميم جذابة. ارتقِ بأسلوبك الطباعي اليوم!
type: docs
weight: 100
url: /ar/net/aspose.words/font/emboss/
---
## Font.Emboss property

صحيح إذا تم تنسيق الخط على أنه منقوش.

```csharp
public bool Emboss { get; set; }
```

## أمثلة

يوضح كيفية تطبيق تأثيرات النقش/النقش البارز على النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// فيما يلي طريقتان لاستخدام الظلال لتطبيق تأثير ثلاثي الأبعاد على النص.
// 1 - نقش النص لجعله يبدو وكأن الحروف غائرة في الصفحة:
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 - قم بنقش النص لجعله يبدو وكأن الحروف تبرز من الصفحة:
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
