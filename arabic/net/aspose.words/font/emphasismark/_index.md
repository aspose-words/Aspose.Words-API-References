---
title: Font.EmphasisMark
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. الحصول على أو تعيين علامة التأكيد المطبقة على هذا التنسيق.
type: docs
weight: 110
url: /ar/net/aspose.words/font/emphasismark/
---
## Font.EmphasisMark property

الحصول على أو تعيين علامة التأكيد المطبقة على هذا التنسيق.

```csharp
public EmphasisMark EmphasisMark { get; set; }
```

### أمثلة

يوضح كيفية إضافة حرف إضافي مقدم أعلى / أسفل الحرف الرسومي.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// الأنواع الممكنة من علامة التركيز:
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
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


