---
title: "طريقة Aspose::Words::Paragraph::get_IsFormatRevision"
linktitle: "get_IsFormatRevision"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Paragraph::get_IsFormatRevision. تُرجع true إذا تم تغيير تنسيق الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words/paragraph/get_isformatrevision/
---
## Paragraph::get_IsFormatRevision method


يرجع true إذا تم تغيير تنسيق الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً.

```cpp
bool Aspose::Words::Paragraph::get_IsFormatRevision()
```


## أمثلة



يعرض كيفية التحقق مما إذا كانت الفقرة تعديل تنسيق.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Format revision.docx");

// هذه الفقرة هي تعديل "Format"، والذي يحدث عندما نقوم بتغيير تنسيق النص الموجود
// أثناء تتبع المراجعات في Microsoft Word عبر "Review" -> "Track changes".
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_IsFormatRevision());
```

## انظر أيضًا

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
