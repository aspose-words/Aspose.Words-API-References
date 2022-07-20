---
title: IsFormatRevision
second_title: Aspose.Words لمراجع .NET API
description: إرجاع صحيح إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تعقب التغييرات.
type: docs
weight: 90
url: /ar/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

إرجاع صحيح إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تعقب التغييرات.

```csharp
public bool IsFormatRevision { get; }
```

### أمثلة

يوضح كيفية التحقق مما إذا كانت الفقرة عبارة عن مراجعة للتنسيق.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// هذه الفقرة هي مراجعة "التنسيق" ، والتي تحدث عندما نغير تنسيق النص الحالي
// أثناء تتبع المراجعات في Microsoft Word عبر "مراجعة" - >; "تعقب التغيرات".
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### أنظر أيضا

* class [Paragraph](../../paragraph)
* مساحة الاسم [Aspose.Words](../../paragraph)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->