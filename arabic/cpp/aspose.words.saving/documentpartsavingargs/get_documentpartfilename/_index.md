---
title: "طريقة Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName"
linktitle: "get_DocumentPartFileName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName. يحصل على اسم الملف (بدون مسار) أو يحدده حيث سيتم حفظ جزء المستند في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartfilename/
---
## DocumentPartSavingArgs::get_DocumentPartFileName method


يحصل أو يعيّن اسم الملف (بدون المسار) حيث سيتم حفظ جزء المستند.

```cpp
System::String Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName() const
```

## ملاحظات


تتيح لك هذه الخاصية إعادة تعريف كيفية إنشاء أسماء ملفات أجزاء المستند أثناء التصدير إلى HTML أو EPUB.

عند استدعاء الدالة الراجعة، تحتوي هذه الخاصية على اسم الملف الذي تم إنشاؤه بواسطة Aspose.Words. يمكنك تغيير قيمة هذه الخاصية لحفظ جزء المستند في ملف مختلف. لاحظ أن اسم الملف لكل جزء يجب أن يكون فريدًا.

[DocumentPartFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name. If output document file name was not specified, for instance when saving to a stream, this file name is used only for referencing document parts. The same is true when saving to EPUB format.

## انظر أيضًا

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
