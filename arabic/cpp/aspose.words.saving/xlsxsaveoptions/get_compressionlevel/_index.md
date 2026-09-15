---
title: "طريقة Aspose::Words::Saving::XlsxSaveOptions::get_CompressionLevel"
linktitle: "get_CompressionLevel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::XlsxSaveOptions::get_CompressionLevel. يحدد مستوى الضغط المستخدم لحفظ المستند. القيمة الافتراضية هي Normal في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.saving/xlsxsaveoptions/get_compressionlevel/
---
## XlsxSaveOptions::get_CompressionLevel method


يحدد مستوى الضغط المستخدم لحفظ المستند. القيمة الافتراضية هي [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::XlsxSaveOptions::get_CompressionLevel() const
```


## أمثلة



يظهر كيفية ضغط مستند XLSX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);
xlsxSaveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Xlsx);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

## انظر أيضًا

* Enum [CompressionLevel](../../compressionlevel/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
