---
title: "طريقة Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName"
linktitle: "get_ExportGeneratorName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName. عندما تكون true، يتسبب في تضمين اسم وإصدار Aspose.Words في الملفات المُنتجة. القيمة الافتراضية هي true في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.saving/saveoptions/get_exportgeneratorname/
---
## SaveOptions::get_ExportGeneratorName method


عند **true**، يتسبب ذلك في تضمين اسم وإصدار Aspose.Words في الملفات المنتجة. القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName() const
```


## أمثلة



يوضح كيفية تعطيل إضافة اسم وإصدار Aspose.Words إلى الملفات المُنتجة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// استخدم https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ لمعرفة كيفية التحقق من النتيجة.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_ExportGeneratorName(false);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

## انظر أيضًا

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
