---
title: Bold
second_title: Aspose.Words لمراجع .NET API
description: True إذا كان تنسيق الخط عريض .
type: docs
weight: 40
url: /ar/net/aspose.words/font/bold/
---
## Font.Bold property

True إذا كان تنسيق الخط عريض .

```csharp
public bool Bold { get; set; }
```

### أمثلة

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد تنسيق الخط ، ثم أضف نصًا.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### أنظر أيضا

* class [Font](../../font)
* مساحة الاسم [Aspose.Words](../../font)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
