---
title: Font.EmphasisMark
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words لـ .NET
description: Font EmphasisMark ملكية. الحصول على أو تعيين علامة التركيز المطبقة على هذا التنسيق في C#.
type: docs
weight: 110
url: /ar/net/aspose.words/font/emphasismark/
---
## Font.EmphasisMark property

الحصول على أو تعيين علامة التركيز المطبقة على هذا التنسيق.

```csharp
public EmphasisMark EmphasisMark { get; set; }
```

## أمثلة

يوضح كيفية إضافة حرف إضافي معروض أعلى/أسفل الحرف الرسومي.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// الأنواع المحتملة لعلامة التركيز:
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
