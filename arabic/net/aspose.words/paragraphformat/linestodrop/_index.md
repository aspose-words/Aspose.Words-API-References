---
title: ParagraphFormat.LinesToDrop
linktitle: LinesToDrop
articleTitle: LinesToDrop
second_title: Aspose.Words لـ .NET
description: ParagraphFormat LinesToDrop ملكية. الحصول على أو تعيين عدد أسطر نص الفقرة المستخدم لحساب ارتفاع الأحرف الاستهلالية في C#.
type: docs
weight: 210
url: /ar/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

الحصول على أو تعيين عدد أسطر نص الفقرة المستخدم لحساب ارتفاع الأحرف الاستهلالية.

```csharp
public int LinesToDrop { get; set; }
```

## أمثلة

يوضح كيفية ضبط حجم الغطاء المنسدل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعديل خاصية "LinesToDrop" لتعيين فقرة كحرف استهلالي منسدل،
// والذي سيحوله إلى حرف كبير كبير يزين الفقرة التالية.
// أعط هذه الخاصية قيمة 4 لإعطاء الأحرف الاستهلالية ارتفاع أربعة أسطر نصية.
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// أعد تعيين خاصية "LinesToDrop" إلى 0 لتحويل الفقرة التالية إلى فقرة عادية.
// سيتم التفاف النص الموجود في هذه الفقرة حول الحرف الاستهلالي المسقط.
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
