---
title: Font.EmphasisMark
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام خاصية "علامة توكيد الخط" لتحسين تنسيق نصك. تعلّم كيفية تعيين علامات التوكيد وتخصيصها لتحسين قابلية القراءة.
type: docs
weight: 110
url: /ar/net/aspose.words/font/emphasismark/
---
## Font.EmphasisMark property

يحصل على علامة التأكيد المطبقة على هذا التنسيق أو يعينها.

```csharp
public EmphasisMark EmphasisMark { get; set; }
```

## أمثلة

يوضح كيفية إضافة حرف إضافي يتم عرضه أعلى/أسفل الحرف الرسومي.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// أنواع علامات التأكيد المحتملة:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder.Font.EmphasisMark = emphasisMark; 

builder.Write("Emphasis text");
builder.Writeln();
builder.Font.ClearFormatting();
builder.Write("Simple text");

builder.Document.Save(ArtifactsDir + "Fonts.SetEmphasisMark.docx");
```

### أنظر أيضا

* enum [EmphasisMark](../../emphasismark/)
* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
