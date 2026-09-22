---
title: "طريقة Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream"
linktitle: "get_ResourceStream"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream. يسمح بتحديد الدفق الذي سيتم حفظ المورد فيه في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.saving/resourcesavingargs/get_resourcestream/
---
## ResourceSavingArgs::get_ResourceStream method


يسمح بتحديد الدفق الذي سيتم حفظ المورد فيه.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream() const
```

## ملاحظات


هذه الخاصية تسمح لك بحفظ الموارد إلى تدفقات بدلاً من ملفات.

القيمة الافتراضية هي **null**. عندما تكون هذه الخاصية **null**، سيتم حفظ المورد إلى ملف محدد في الخاصية [ResourceFileName](../get_resourcefilename/).

باستخدام [IResourceSavingCallback](../../iresourcesavingcallback/) لا يمكنك استبدال مورد بآخر. يُقصد به فقط التحكم في الموقع الذي تُحفظ فيه الموارد.

## انظر أيضًا

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
