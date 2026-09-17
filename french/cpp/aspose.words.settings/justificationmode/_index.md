---
title: "Aspose::Words::Settings::JustificationMode enum"
linktitle: "JustificationMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Settings::JustificationMode enum. Spécifie l'ajustement de l'espacement des caractères pour un document. La valeur par défaut est Expand en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.settings/justificationmode/
---
## JustificationMode enum


Spécifie le réglage de l'espacement des caractères pour un document. La valeur par défaut est **Expand**.

```cpp
enum class JustificationMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Expand | 0 | Ne pas compresser l'espacement des caractères. |
| Compress | 1 | Compresser l'espacement des caractères. |
| CompressKana | 2 | Compresser, en utilisant les règles des syllabaires kana, Hiragana et Katakana. |


## Exemples



Montre comment gérer le contrôle de l'espacement des caractères.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

Aspose::Words::Settings::JustificationMode justificationMode = doc->get_JustificationMode();
if (justificationMode == Aspose::Words::Settings::JustificationMode::Expand)
{
    doc->set_JustificationMode(Aspose::Words::Settings::JustificationMode::Compress);
}

doc->Save(get_ArtifactsDir() + u"Document.SetJustificationMode.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
