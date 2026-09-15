---
title: "منشئ ChmLoadOptions في Aspose::Words::Loading::ChmLoadOptions"
linktitle: "ChmLoadOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ ChmLoadOptions في Aspose::Words::Loading::ChmLoadOptions. يقوم بإنشاء نسخة جديدة من هذه الفئة بالقيم الافتراضية في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions::ChmLoadOptions constructor


ينشئ نسخة جديدة من هذه الفئة بالقيم الافتراضية.

```cpp
Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions()
```


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
