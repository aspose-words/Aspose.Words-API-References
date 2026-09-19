---
title: "Aspose::Words::Settings::JustificationMode enum"
linktitle: "JustificationMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Settings::JustificationMode enum. Specifica la regolazione della spaziatura dei caratteri per un documento. Il valore predefinito è Expand in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.settings/justificationmode/
---
## JustificationMode enum


Specifica la regolazione della spaziatura dei caratteri per un documento. Il valore predefinito è **Expand**.

```cpp
enum class JustificationMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Expand | 0 | Non comprimere la spaziatura dei caratteri. |
| Compress | 1 | Comprimi la spaziatura dei caratteri. |
| CompressKana | 2 | Comprimi, usando le regole delle sillabari kana, Hiragana e Katakana. |


## Esempi



Mostra come gestire il controllo della spaziatura dei caratteri.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

Aspose::Words::Settings::JustificationMode justificationMode = doc->get_JustificationMode();
if (justificationMode == Aspose::Words::Settings::JustificationMode::Expand)
{
    doc->set_JustificationMode(Aspose::Words::Settings::JustificationMode::Compress);
}

doc->Save(get_ArtifactsDir() + u"Document.SetJustificationMode.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
