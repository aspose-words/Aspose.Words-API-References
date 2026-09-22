---
title: "طريقة Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri"
linktitle: "get_ResourceFileUri"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri. يحصل على أو يضبط معرف الموارد الموحد (URI) المستخدم للإشارة إلى ملف المورد من المستند في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.saving/resourcesavingargs/get_resourcefileuri/
---
## ResourceSavingArgs::get_ResourceFileUri method


يحصل أو يعيّن معرف المورد الموحد (URI) المستخدم للإشارة إلى ملف المورد من المستند.

```cpp
System::String Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri() const
```

## ملاحظات


تسمح لك هذه الخاصية بتغيير عناوين URI لملفات الموارد المصدرة إلى مستندات HTML ثابت الصفحات أو SVG أو Markdown.

يقوم Aspose.Words تلقائيًا بإنشاء URI لكل ملف مورد أثناء التصدير إلى تنسيق HTML ثابت الصفحات أو SVG أو Markdown. تشير عناوين URI المُنشأة إلى ملفات الموارد التي حفظها Aspose.Words. ومع ذلك، قد تكون عناوين URI غير صحيحة إذا تم نقل ملفات الموارد إلى موقع آخر أو إذا تم حفظ ملفات الموارد إلى تدفقات. تسمح لك هذه الخاصية بتصحيح عناوين URI في هذه الحالات.

عند حدوث الحدث، تحتوي هذه الخاصية على URI الذي تم إنشاؤه بواسطة Aspose.Words. يمكنك تغيير قيمة هذه الخاصية لتوفير URI مخصص لملف المورد.
## انظر أيضًا

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
