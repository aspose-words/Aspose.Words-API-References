---
title: Font.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words لـ .NET
description: Font Shadow ملكية. صحيح إذا تم تنسيق الخط على أنه مظلل في C#.
type: docs
weight: 330
url: /ar/net/aspose.words/font/shadow/
---
## Font.Shadow property

صحيح إذا تم تنسيق الخط على أنه مظلل.

```csharp
public bool Shadow { get; set; }
```

## أمثلة

يوضح كيفية إنشاء سلسلة نص منسقة بظل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// اضبط علامة الظل لتطبيق تأثير ظل الإزاحة،
// جعل الحروف تبدو وكأنها تطفو فوق الصفحة.
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
