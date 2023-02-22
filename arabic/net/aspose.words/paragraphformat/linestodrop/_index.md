---
title: ParagraphFormat.LinesToDrop
second_title: Aspose.Words لمراجع .NET API
description: ParagraphFormat ملكية. الحصول على أو تحديد عدد سطور نص الفقرة المستخدم لحساب ارتفاع الحرف الاستهلالي .
type: docs
weight: 200
url: /ar/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

الحصول على أو تحديد عدد سطور نص الفقرة المستخدم لحساب ارتفاع الحرف الاستهلالي .

```csharp
public int LinesToDrop { get; set; }
```

### أمثلة

يوضح كيفية تعيين حجم الحد الأقصى المسقط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعديل خاصية "LinesToDrop" لتعيين فقرة على أنها حرف استهلالي كبير ،
// الذي سيحوله إلى حرف كبير كبير يزين الفقرة التالية.
// أعط هذه الخاصية قيمة 4 لمنح الحرف الاستهلالي ارتفاع أربعة أسطر نصية.
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// إعادة تعيين خاصية "LinesToDrop" إلى 0 لتحويل الفقرة التالية إلى فقرة عادية.
// سيتم التفاف النص في هذه الفقرة حول الأحرف الاستهلالية الكبيرة.
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../paragraphformat/)
* المجسم [Aspose.Words](../../../)


