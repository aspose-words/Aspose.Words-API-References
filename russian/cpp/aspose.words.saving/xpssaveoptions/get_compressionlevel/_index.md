---
title: "Метод Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel"
linktitle: "get_CompressionLevel"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel. Указывает уровень сжатия, используемый при сохранении документа. Значение по умолчанию — Normal в C++."
type: docs
weight: 2250
url: /ru/cpp/aspose.words.saving/xpssaveoptions/get_compressionlevel/
---
## XpsSaveOptions::get_CompressionLevel method


Указывает уровень сжатия, используемый при сохранении документа. Значение по умолчанию — [Normal](../../compressionlevel/).

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel() const
```


## Примеры



Показывает, как управлять уровнем сжатия при сохранении документа в формат XPS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// Создайте объект XpsSaveOptions и задайте уровень сжатия.
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## См. также

* Enum [CompressionLevel](../../compressionlevel/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
