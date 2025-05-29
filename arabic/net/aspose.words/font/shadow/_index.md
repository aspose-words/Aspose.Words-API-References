---
title: Font.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Font Shadow، وقم بتعزيز نصك باستخدام تأثيرات الظل الأنيقة للحصول على جاذبية بصرية مذهلة في تصميماتك.
type: docs
weight: 340
url: /ar/net/aspose.words/font/shadow/
---
## Font.Shadow property

صحيح إذا تم تنسيق الخط على أنه مظلل.

```csharp
public bool Shadow { get; set; }
```

## أمثلة

يوضح كيفية إنشاء سلسلة من النص منسقة بظل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// اضبط علم الظل لتطبيق تأثير الظل الإزاحي،
// مما يجعل الأمر يبدو وكأن الحروف تطفو فوق الصفحة.
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
