---
title: Font.Bold
linktitle: Bold
articleTitle: Bold
second_title: Aspose.Words لـ .NET
description: Font Bold ملكية. صحيح إذا كان الخط منسقًا بالخط الغامق في C#.
type: docs
weight: 40
url: /ar/net/aspose.words/font/bold/
---
## Font.Bold property

صحيح إذا كان الخط منسقًا بالخط الغامق.

```csharp
public bool Bold { get; set; }
```

## أمثلة

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد تنسيق الخط، ثم أضف النص.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
