---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat метод"
linktitle: "get_SaveFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat метод. Указывает формат, в котором будет сохранён документ, если используется этот объект параметров сохранения. Может быть только Xlsx в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/xlsxsaveoptions/get_saveformat/
---
## XlsxSaveOptions::get_SaveFormat method


Указывает формат, в котором будет сохранён документ, если используется этот объект параметров сохранения. Может быть только [Xxlsx](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat() override
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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
