---
title: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData method"
linktitle: "get_IgnoreOleData"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData method. يحدد ما إذا كان يجب تجاهل بيانات OLE في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.loading/loadoptions/get_ignoreoledata/
---
## LoadOptions::get_IgnoreOleData method


يحدد ما إذا كان يجب تجاهل بيانات OLE.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_IgnoreOleData() const
```

## ملاحظات


قد يؤدي تجاهل بيانات OLE إلى تقليل استهلاك الذاكرة وزيادة الأداء دون فقدان البيانات في حالة عدم دعم تنسيق الوجهة لكائنات OLE.

القيمة الافتراضية هي **false**.

## أمثلة



يوضح كيفية تجاهل بيانات OLE أثناء التحميل.
```cpp
// قد يؤدي تجاهل بيانات OLE إلى تقليل استهلاك الذاكرة وزيادة الأداء
// دون فقدان البيانات في حالة عدم دعم تنسيق الوجهة لكائنات OLE.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_IgnoreOleData(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE objects.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.IgnoreOleData.docx");
```

## انظر أيضًا

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
