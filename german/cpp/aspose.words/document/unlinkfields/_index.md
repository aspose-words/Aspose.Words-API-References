---
title: "Aspose::Words::Document::UnlinkFields Methode"
linktitle: "UnlinkFields"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::UnlinkFields Methode. Löst Feldverknüpfungen im gesamten Dokument in C++."
type: docs
weight: 94000
url: /de/cpp/aspose.words/document/unlinkfields/
---
## Document::UnlinkFields method


Entkoppelt Felder im gesamten Dokument.

```cpp
void Aspose::Words::Document::UnlinkFields()
```

## Hinweise


Ersetzt alle Felder im gesamten Dokument durch deren aktuellste Ergebnisse.

Um Felder in einem bestimmten Teil des Dokuments zu entkoppeln, verwenden Sie [UnlinkFields](../../range/unlinkfields/).

## Beispiele



Zeigt, wie man alle Felder im Dokument entkoppelt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

doc->UnlinkFields();
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
