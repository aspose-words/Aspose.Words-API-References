---
title: "Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields-Methode"
linktitle: "get_PreserveFormFields"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields-Methode. Gibt an, ob Microsoft‑Word‑Formularfelder als Formularfelder im PDF erhalten oder in Text konvertiert werden sollen. Standard ist **false** in C++."
type: docs
weight: 28000
url: /de/cpp/aspose.words.saving/pdfsaveoptions/get_preserveformfields/
---
## PdfSaveOptions::get_PreserveFormFields method


Gibt an, ob Microsoft Word-Formularfelder als Formularfelder im PDF erhalten bleiben oder in Text konvertiert werden sollen. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields() const
```

## Hinweise


Microsoft‑Word‑Formularfelder umfassen Texteingaben, Dropdown‑ und Kontrollkästchen‑Steuerelemente.

Wenn sie auf **false** gesetzt sind, werden diese Felder als Text in das PDF exportiert. Wenn sie auf **true** gesetzt sind, werden diese Felder als PDF‑Formularfelder exportiert.

Beim Exportieren von Formularfeldern als PDF‑Formularfelder kann es zu einem gewissen Formatierungsverlust kommen, da PDF‑Formularfelder nicht alle Funktionen von Microsoft‑Word‑Formularfeldern unterstützen.

Außerdem hängt die Ausgabedateigröße von der Inhaltsgröße ab, da editierbare Formulare in Microsoft Word Inline‑Objekte sind.
## Siehe auch

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
