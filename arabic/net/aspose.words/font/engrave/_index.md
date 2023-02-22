---
title: Font.Engrave
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. صحيح إذا تم تنسيق الخط على أنه محفور.
type: docs
weight: 120
url: /ar/net/aspose.words/font/engrave/
---
## Font.Engrave property

صحيح إذا تم تنسيق الخط على أنه محفور.

```csharp
public bool Engrave { get; set; }
```

### أمثلة

يوضح كيفية تطبيق تأثيرات النقش / النقش على النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// فيما يلي طريقتان لاستخدام الظلال لتطبيق تأثير ثلاثي الأبعاد على النص.
// 1 - نقش النص لجعله يبدو وكأن الحروف غارقة في الصفحة:
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 - قم بزخرفة النص لجعله يبدو مثل الحروف المنبثقة من الصفحة:
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


