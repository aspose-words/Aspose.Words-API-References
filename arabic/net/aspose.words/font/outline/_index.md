---
title: Font.Outline
linktitle: Outline
articleTitle: Outline
second_title: Aspose.Words لـ .NET
description: Font Outline ملكية. صحيح إذا تم تنسيق الخط كمخطط تفصيلي في C#.
type: docs
weight: 290
url: /ar/net/aspose.words/font/outline/
---
## Font.Outline property

صحيح إذا تم تنسيق الخط كمخطط تفصيلي.

```csharp
public bool Outline { get; set; }
```

## أمثلة

يوضح كيفية إنشاء مجموعة من النص المنسق كمخطط تفصيلي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتعيين علامة المخطط التفصيلي لتغيير لون تعبئة النص إلى اللون الأبيض و
 // اترك مخططًا رفيعًا حول كل حرف باللون الأصلي للنص.
builder.Font.Outline = true;
builder.Font.Color = Color.Blue;
builder.Font.Size = 36;

builder.Writeln("This text has an outline.");

doc.Save(ArtifactsDir + "Font.Outline.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
