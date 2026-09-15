---
title: "طريقة Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles"
linktitle: "get_AlwaysCompressMetafiles"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles. عندما تكون false، لا يتم ضغط ملفات الميتا الصغيرة لأسباب تتعلق بالأداء. القيمة الافتراضية هي true، جميع ملفات الميتا تُضغط بغض النظر عن حجمها في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.saving/docsaveoptions/get_alwayscompressmetafiles/
---
## DocSaveOptions::get_AlwaysCompressMetafiles method


عند **false**، لا يتم ضغط ملفات الميتا الصغيرة لأسباب تتعلق بالأداء. القيمة الافتراضية هي **true**، جميع ملفات الميتا تُضغط بغض النظر عن حجمها.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles() const
```


## أمثلة



يوضح كيفية تغيير ضغط ملفات الميتا في مستند أثناء الحفظ.
```cpp
// افتح مستندًا يحتوي على صيغة Microsoft Equation 3.0.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Microsoft equation object.docx");

// عند حفظ مستند، لا يتم ضغط ملفات الميتا الصغيرة لأسباب تتعلق بالأداء.
// يمكننا تعيين علامة في كائن SaveOptions لضغط كل ملف ميتا عند الحفظ.
// بعض المحررات مثل LibreOffice لا يمكنها قراءة ملفات الميتا غير المضغوطة.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_AlwaysCompressMetafiles(compressAllMetafiles);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

## انظر أيضًا

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
