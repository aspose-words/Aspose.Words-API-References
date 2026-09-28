---
title: "Метод Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName"
linktitle: "get_ExportGeneratorName"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName. Когда значение истинно, имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию — true в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.saving/saveoptions/get_exportgeneratorname/
---
## SaveOptions::get_ExportGeneratorName method


Когда **true**, имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию — **true**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName() const
```


## Примеры



Показывает, как отключить добавление имени и версии Aspose.Words в создаваемые файлы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Используйте https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ чтобы узнать, как проверить результат.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_ExportGeneratorName(false);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

## См. также

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
