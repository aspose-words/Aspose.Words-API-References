---
title: "Aspose::Words::Saving::XlsxSectionMode перечисление"
linktitle: "XxlsxSectionMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::XlsxSectionMode перечисление. Указывает, как обрабатываются разделы при сохранении документа в формате XLSX в C++."
type: docs
weight: 87000
url: /ru/cpp/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enum


Указывает, как разделы обрабатываются при сохранении документа в формате XLSX.

```cpp
enum class XlsxSectionMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| MultipleWorksheets | 0 | Указывает, что отдельный лист создаётся для каждого раздела документа. |
| SingleWorksheet | 1 | Указывает, что все разделы документа сохраняются на одном листе. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
