---
title: Font.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية تظليل الخط، التي توفر كائن تظليل لتنسيق الخط القابل للتخصيص، مما يعزز من جاذبية النص المرئية.
type: docs
weight: 330
url: /ar/net/aspose.words/font/shading/
---
## Font.Shading property

يعيد[`Shading`](../../shading/) كائن يشير إلى تنسيق التظليل للخط.

```csharp
public Shading Shading { get; }
```

## أمثلة

يوضح كيفية تطبيق التظليل على النص الذي تم إنشاؤه بواسطة منشئ المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Color = Color.White;

// إحدى الطرق لجعل النص الذي تم إنشاؤه باستخدام لون الخط الأبيض مرئيًا
// هو تطبيق تأثير التظليل في الخلفية.
Shading shading = builder.Font.Shading;
shading.Texture = TextureIndex.TextureDiagonalUp;
shading.BackgroundPatternColor = Color.OrangeRed;
shading.ForegroundPatternColor = Color.DarkBlue;

builder.Writeln("White text on an orange background with a two-tone texture.");

doc.Save(ArtifactsDir + "Font.Shading.docx");
```

### أنظر أيضا

* class [Shading](../../shading/)
* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
