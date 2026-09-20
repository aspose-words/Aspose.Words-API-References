---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode метод"
linktitle: "get_SectionMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode. Получает или задает способ обработки разделов при сохранении в выходной документ XLSX. Значение по умолчанию — MultipleWorksheets в C++."
type: docs
weight: 4500
url: /ru/cpp/aspose.words.saving/xlsxsaveoptions/get_sectionmode/
---
## XlsxSaveOptions::get_SectionMode method


Получает или задает способ обработки разделов при сохранении в выходной документ XLSX. Значение по умолчанию — [MultipleWorksheets](../../xlsxsectionmode/).

```cpp
Aspose::Words::Saving::XlsxSectionMode Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode() const
```


## Примеры



Показывает, как сохранить документ в виде отдельных листов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// Каждый раздел документа будет создан как отдельный лист.
// Используйте 'SingleWorksheet', чтобы отобразить весь документ на одном листе.
auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_SectionMode(Aspose::Words::Saving::XlsxSectionMode::MultipleWorksheets);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

## См. также

* Enum [XlsxSectionMode](../../xlsxsectionmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
