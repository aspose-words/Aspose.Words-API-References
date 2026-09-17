---
title: "Aspose::Words::Document::get_JustificationMode méthode"
linktitle: "get_JustificationMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_JustificationMode méthode. Obtient ou définit l'ajustement de l'espacement des caractères d'un document en C++."
type: docs
weight: 34000
url: /fr/cpp/aspose.words/document/get_justificationmode/
---
## Document::get_JustificationMode method


Obtient ou définit le réglage de l'espacement des caractères d'un document.

```cpp
Aspose::Words::Settings::JustificationMode Aspose::Words::Document::get_JustificationMode()
```


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

* Enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
