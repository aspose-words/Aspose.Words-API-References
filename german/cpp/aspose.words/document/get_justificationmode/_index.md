---
title: "Aspose::Words::Document::get_JustificationMode Methode"
linktitle: "get_JustificationMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_JustificationMode Methode. Liest oder setzt die Zeichenabstands-Anpassung eines Dokuments in C++."
type: docs
weight: 34000
url: /de/cpp/aspose.words/document/get_justificationmode/
---
## Document::get_JustificationMode method


Liest oder legt die Zeichenabstandsanpassung eines Dokuments fest.

```cpp
Aspose::Words::Settings::JustificationMode Aspose::Words::Document::get_JustificationMode()
```


## Beispiele



Zeigt, wie die Zeichenabstandskontrolle verwaltet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

Aspose::Words::Settings::JustificationMode justificationMode = doc->get_JustificationMode();
if (justificationMode == Aspose::Words::Settings::JustificationMode::Expand)
{
    doc->set_JustificationMode(Aspose::Words::Settings::JustificationMode::Compress);
}

doc->Save(get_ArtifactsDir() + u"Document.SetJustificationMode.docx");
```

## Siehe auch

* Enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
