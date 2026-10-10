---
title: "Aspose::Words::Range::UnlinkFields Methode"
linktitle: "UnlinkFields"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Range::UnlinkFields Methode. Löst Felder in diesem Bereich in C++."
type: docs
weight: 14000
url: /de/cpp/aspose.words/range/unlinkfields/
---
## Range::UnlinkFields method


Löst die Verknüpfung von Feldern in diesem Bereich.

```cpp
void Aspose::Words::Range::UnlinkFields()
```

## Hinweise


Ersetzt alle Felder in diesem Bereich durch deren aktuellste Ergebnisse.

Um Felder im gesamten Dokument zu lösen, verwenden Sie [UnlinkFields](./).

## Beispiele



Zeigt, wie man alle Felder in einem Bereich löst.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

auto newSection = System::ExplicitCast<Aspose::Words::Section>(System::ExplicitCast<Aspose::Words::Node>(doc->get_Sections()->idx_get(0))->Clone(true));
doc->get_Sections()->Add(newSection);

doc->get_Sections()->idx_get(1)->get_Range()->UnlinkFields();
```

## Siehe auch

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
