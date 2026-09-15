---
title: "طريقة Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName"
linktitle: "get_OriginalFileName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName. اسم ملف CHM. القيمة الافتراضية هي null في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.loading/chmloadoptions/get_originalfilename/
---
## ChmLoadOptions::get_OriginalFileName method


اسم ملف CHM. القيمة الافتراضية هي **null**.

```cpp
System::String Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName() const
```

## ملاحظات


قد تحتوي مستندات CHM على روابط تشير إلى نفس المستند باسم الملف. يدعم Aspose.Words هذه الروابط وعادةً يستخدم [OriginalFileName](../../../aspose.words/document/get_originalfilename/) للتحقق مما إذا كان الملف المشار إليه بالرابط هو الملف الذي يتم تحميله. إذا تم تحميل مستند من تدفق، يجب تحديد اسم الملف الأصلي صراحةً عبر هذه الخاصية، لأنه لا يمكن تحديده تلقائيًا.

إذا تم تحميل مستند CHM من ملف وتم تحديد قيمة غير فارغة لهذه الخاصية، فستأخذ هذه القيمة أولوية على الاسم الفعلي للملف المخزن في [OriginalFileName](../../../aspose.words/document/get_originalfilename/).

## أمثلة



يوضح كيفية حل عناوين URL مثل "ms-its:myfile.chm::/index.htm".
```cpp
// يحتوي مستندنا على عناوين URL مثل "ms-its:amhelp.chm::....htm"، لكنه يحمل اسمًا مختلفًا،
// لذلك لا تعمل روابط الملفات بعد حفظه كـ HTML.
// نحتاج إلى تحديد اسم الملف الأصلي في 'ChmLoadOptions' لتجنب هذا السلوك.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::ChmLoadOptions>();
loadOptions->set_OriginalFileName(u"amhelp.chm");

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::IO::File::ReadAllBytes(get_MyDir() + u"Document with ms-its links.chm")), loadOptions);

doc->Save(get_ArtifactsDir() + u"ExChmLoadOptions.OriginalFileName.html");
```

## انظر أيضًا

* Class [ChmLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
