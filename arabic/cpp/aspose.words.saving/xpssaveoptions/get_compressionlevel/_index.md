---
title: "Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel طريقة"
linktitle: "get_CompressionLevel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel طريقة. يحدد مستوى الضغط المستخدم لحفظ المستند. القيمة الافتراضية هي Normal في C++."
type: docs
weight: 2250
url: /ar/cpp/aspose.words.saving/xpssaveoptions/get_compressionlevel/
---
## XpsSaveOptions::get_CompressionLevel method


يحدد مستوى الضغط المستخدم لحفظ المستند. القيمة الافتراضية هي [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel() const
```


## أمثلة



يظهر كيفية التحكم في مستوى الضغط عند حفظ مستند إلى تنسيق XPS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// أنشئ كائن XpsSaveOptions وحدد مستوى الضغط.
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## انظر أيضًا

* Enum [CompressionLevel](../../compressionlevel/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
