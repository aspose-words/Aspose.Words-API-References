---
title: "Aspose::Words::Document::get_JustificationMode method"
linktitle: "get_JustificationMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_JustificationMode method. Hämtar eller anger teckenavståndsjusteringen för ett dokument i C++."
type: docs
weight: 34000
url: /sv/cpp/aspose.words/document/get_justificationmode/
---
## Document::get_JustificationMode method


Hämtar eller anger teckenavståndsjusteringen för ett dokument.

```cpp
Aspose::Words::Settings::JustificationMode Aspose::Words::Document::get_JustificationMode()
```


## Exempel



Visar hur man hanterar kontroll av teckenavstånd.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

Aspose::Words::Settings::JustificationMode justificationMode = doc->get_JustificationMode();
if (justificationMode == Aspose::Words::Settings::JustificationMode::Expand)
{
    doc->set_JustificationMode(Aspose::Words::Settings::JustificationMode::Compress);
}

doc->Save(get_ArtifactsDir() + u"Document.SetJustificationMode.docx");
```

## Se även

* Enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
