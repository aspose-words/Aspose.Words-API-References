---
title: "Aspose::Words::Settings::JustificationMode enum"
linktitle: "JustificationMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::JustificationMode enum. Указывает настройку межсимвольного интервала для документа. Значение по умолчанию — Expand в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.settings/justificationmode/
---
## JustificationMode enum


Указывает настройку межсимвольного интервала для документа. Значение по умолчанию — **Expand**.

```cpp
enum class JustificationMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Expand | 0 | Не сжимать межсимвольный интервал. |
| Compress | 1 | Сжать межсимвольный интервал. |
| CompressKana | 2 | Сжать, используя правила кана, хираганы и катаканы. |


## Примеры



Показывает, как управлять контролем межсимвольного интервала.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

Aspose::Words::Settings::JustificationMode justificationMode = doc->get_JustificationMode();
if (justificationMode == Aspose::Words::Settings::JustificationMode::Expand)
{
    doc->set_JustificationMode(Aspose::Words::Settings::JustificationMode::Compress);
}

doc->Save(get_ArtifactsDir() + u"Document.SetJustificationMode.docx");
```

## См. также

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
