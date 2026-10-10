---
title: "Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts Methode"
linktitle: "get_GenerateFormFieldScripts"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts Methode. Gibt an, ob Skripte erzeugt werden sollen, die das spezifische Verhalten von Microsoft‑Word-Formularfeldern in PDF nachahmen. Standardwert ist false in C++."
type: docs
weight: 18500
url: /de/cpp/aspose.words.saving/pdfsaveoptions/get_generateformfieldscripts/
---
## PdfSaveOptions::get_GenerateFormFieldScripts method


Gibt an, ob Skripte erzeugt werden sollen, die das Verhalten bestimmter Microsoft‑Word‑Formularfeld‑Funktionen in PDF emulieren. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts() const
```

## Hinweise


Wenn diese Option aktiviert ist, erzeugt der Exporter PDF‑JavaScript‑Aktionen, um das Verhalten von Microsoft‑Word‑Formularfeldern nachzuahmen, z. B. Datums‑ und Zeitformularfelder mit Formatierungs‑ und Validierungsregeln.

Wenn auf **true** gesetzt, wird das unterstützte Verhalten als PDF‑JavaScript‑Aktionen exportiert. Wenn auf **false** gesetzt, werden keine Formularfeld‑Skripte erzeugt.

Die Skriptausführung hängt vom PDF‑Betrachter ab. Einige PDF‑Betrachter können Skripte ignorieren, die Skriptausführung einschränken oder erfordern, dass der Benutzer JavaScript aktiviert.

JavaScript‑Aktionen sind durch die PDF/A‑1-, PDF/A‑2- und PDF/A‑3‑Konformität verboten. Der Wert **false** wird in diesem Fall automatisch verwendet.
## Siehe auch

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
