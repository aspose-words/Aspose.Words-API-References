---
title: Paragraph.IsFormatRevision
linktitle: IsFormatRevision
articleTitle: IsFormatRevision
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تقوم خاصية IsFormatRevision في Microsoft Word بتتبع تغييرات التنسيق، مما يضمن تحرير المستندات بدقة وتعزيز التعاون.
type: docs
weight: 90
url: /ar/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

يعود صحيحًا إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تتبع التغييرات.

```csharp
public bool IsFormatRevision { get; }
```

## أمثلة

يوضح كيفية التحقق مما إذا كانت الفقرة عبارة عن مراجعة تنسيق.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// هذه الفقرة هي مراجعة "تنسيق"، والتي تحدث عندما نقوم بتغيير تنسيق النص الموجود
// أثناء تتبع المراجعات في Microsoft Word عبر "مراجعة" -> "تتبع التغييرات".
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### أنظر أيضا

* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
