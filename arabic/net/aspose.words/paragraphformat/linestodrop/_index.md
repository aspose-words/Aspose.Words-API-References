---
title: ParagraphFormat.LinesToDrop
linktitle: LinesToDrop
articleTitle: LinesToDrop
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية ParagraphFormat LinesToDrop ارتفاع الأحرف الكبيرة في مستنداتك. حسّن تصميم نصك للحصول على صور مذهلة!
type: docs
weight: 210
url: /ar/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

يحصل على عدد أسطر نص الفقرة المستخدمة لحساب ارتفاع الحرف الكبير أو يعينه.

```csharp
public int LinesToDrop { get; set; }
```

## أمثلة

يوضح كيفية ضبط حجم الحرف الكبير.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعديل خاصية "LinesToDrop" لتعيين فقرة كحرف كبير منسدلة،
// مما سيحوله إلى حرف كبير يزين الفقرة التالية.
// أعط هذه الخاصية قيمة 4 لإعطاء الحرف الكبير ارتفاع أربعة أسطر نصية.
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// قم بإعادة تعيين خاصية "LinesToDrop" إلى 0 لتحويل الفقرة التالية إلى فقرة عادية.
//سيتم لف النص الموجود في هذه الفقرة حول الحرف الكبير المنسدل.
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
