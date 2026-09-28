---
title: "Aspose::Words::Saving::TxtOfficeMathExportMode enum"
linktitle: "TxtOfficeMathExportMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::TxtOfficeMathExportMode enum. Указывает, как Aspose.Words экспортирует OfficeMath в текст в C++."
type: docs
weight: 86250
url: /ru/cpp/aspose.words.saving/txtofficemathexportmode/
---
## TxtOfficeMathExportMode enum


Указывает, как Aspose.Words экспортирует OfficeMath в [Text](../../aspose.words/saveformat/).

```cpp
enum class TxtOfficeMathExportMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Text | 0 | Экспортировать OfficeMath как простой текст. |
| Latex | 3 | Экспортировать OfficeMath как LaTeX. |


## Примеры



Показывает, как экспортировать объект OfficeMath как Latex в TXT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
