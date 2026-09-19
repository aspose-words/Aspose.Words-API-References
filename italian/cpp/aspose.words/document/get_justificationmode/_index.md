---
title: "Metodo Aspose::Words::Document::get_JustificationMode"
linktitle: "get_JustificationMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::get_JustificationMode. Ottiene o imposta la regolazione della spaziatura dei caratteri di un documento in C++."
type: docs
weight: 34000
url: /it/cpp/aspose.words/document/get_justificationmode/
---
## Document::get_JustificationMode method


Ottiene o imposta la regolazione della spaziatura dei caratteri di un documento.

```cpp
Aspose::Words::Settings::JustificationMode Aspose::Words::Document::get_JustificationMode()
```


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

* Enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
