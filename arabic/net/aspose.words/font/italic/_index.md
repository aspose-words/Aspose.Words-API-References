---
title: Font.Italic
linktitle: Italic
articleTitle: Italic
second_title: Aspose.Words لـ .NET
description: Font Italic ملكية. صحيح إذا كان الخط منسقًا بالخط المائل في C#.
type: docs
weight: 160
url: /ar/net/aspose.words/font/italic/
---
## Font.Italic property

صحيح إذا كان الخط منسقًا بالخط المائل.

```csharp
public bool Italic { get; set; }
```

## أمثلة

يوضح كيفية كتابة نص مائل باستخدام أداة إنشاء المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Italic = true;
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "Font.Italic.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
