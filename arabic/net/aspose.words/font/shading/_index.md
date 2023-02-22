---
title: Font.Shading
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. إرجاع كائن تظليل يشير إلى تنسيق التظليل للخط.
type: docs
weight: 320
url: /ar/net/aspose.words/font/shading/
---
## Font.Shading property

إرجاع كائن تظليل يشير إلى تنسيق التظليل للخط.

```csharp
public Shading Shading { get; }
```

### أمثلة

يوضح كيفية تطبيق التظليل على النص الذي تم إنشاؤه بواسطة منشئ المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Color = Color.White;

// طريقة واحدة لجعل النص الذي تم إنشاؤه باستخدام لون الخط الأبيض مرئيًا
// هو تطبيق تأثير تظليل الخلفية.
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
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


