---
title: Font.Shadow
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. True إذا تم تنسيق الخط على أنه مظلل .
type: docs
weight: 330
url: /ar/net/aspose.words/font/shadow/
---
## Font.Shadow property

True إذا تم تنسيق الخط على أنه مظلل .

```csharp
public bool Shadow { get; set; }
```

### أمثلة

يوضح كيفية إنشاء سلسلة من النص المنسق بظل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// اضبط علامة الظل لتطبيق تأثير ظل الإزاحة ،
// مما يجعلها تبدو وكأن الأحرف تطفو فوق الصفحة.
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


