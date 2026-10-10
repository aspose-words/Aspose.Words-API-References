---
title: "Aspose::Words::Settings::JustificationMode enum"
linktitle: "JustificationMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::JustificationMode enum. Anger justering av teckenavstånd för ett dokument. Standardvärdet är Expand i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words.settings/justificationmode/
---
## JustificationMode enum


Anger teckenavståndsjusteringen för ett dokument. Standardvärdet är **Expand**.

```cpp
enum class JustificationMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Expand | 0 | Komprimera inte teckenavstånd. |
| Compress | 1 | Komprimera teckenavstånd. |
| CompressKana | 2 | Komprimera, med hjälp av regler för kana-syllabaries, Hiragana och Katakana. |


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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
