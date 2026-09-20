---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_CompressionLevel метод"
linktitle: "get_CompressionLevel"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_CompressionLevel метод. Указывает уровень сжатия, используемый при сохранении документа. Значение по умолчанию — Normal в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.saving/xlsxsaveoptions/get_compressionlevel/
---
## XlsxSaveOptions::get_CompressionLevel method


Указывает уровень сжатия, используемый при сохранении документа. Значение по умолчанию — [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::XlsxSaveOptions::get_CompressionLevel() const
```


## Примеры



Показывает, как сжать документ XLSX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);
xlsxSaveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Xlsx);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

## См. также

* Enum [CompressionLevel](../../compressionlevel/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
