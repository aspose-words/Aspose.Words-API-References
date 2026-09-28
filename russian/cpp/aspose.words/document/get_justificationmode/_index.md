---
title: "Метод Aspose::Words::Document::get_JustificationMode"
linktitle: "get_JustificationMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::get_JustificationMode. Получает или задает настройку межсимвольного интервала документа в C++."
type: docs
weight: 34000
url: /ru/cpp/aspose.words/document/get_justificationmode/
---
## Document::get_JustificationMode method


Получает или задает корректировку межсимвольного интервала документа.

```cpp
Aspose::Words::Settings::JustificationMode Aspose::Words::Document::get_JustificationMode()
```


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

* Enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
