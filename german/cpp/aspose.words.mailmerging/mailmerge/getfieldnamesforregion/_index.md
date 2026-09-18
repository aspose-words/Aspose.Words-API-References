---
title: "Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion Methode"
linktitle: "GetFieldNamesForRegion"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion Methode. Gibt eine Sammlung von Mail‑Merge‑Feldnamen zurück, die in der Region in C++ verfügbar sind."
type: docs
weight: 22000
url: /de/cpp/aspose.words.mailmerging/mailmerge/getfieldnamesforregion/
---
## MailMerge::GetFieldNamesForRegion(const System::String\&) method


Gibt eine Sammlung von Seriendruckfeldnamen zurück, die in der Region verfügbar sind.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| regionName | const System::String\& | Regionname (Groß-/Kleinschreibung wird ignoriert). |
## Hinweise


Gibt vollständige Merge‑Feldnamen einschließlich optionalem Präfix zurück. Entfernt keine doppelten Feldnamen.

Wenn das Dokument mehrere Regionen mit demselben Namen enthält, wird die allererste Region verarbeitet.

Bei jedem Aufruf wird ein neues String‑Array erstellt.

## Siehe auch

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::GetFieldNamesForRegion(const System::String\&, int32_t) method


Gibt eine Sammlung von Seriendruckfeldnamen zurück, die in der Region verfügbar sind.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName, int32_t regionIndex)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| regionName | const System::String\& | Regionname (Groß-/Kleinschreibung wird ignoriert). |
| regionIndex | int32_t | Regionindex (nullbasiert). |
## Hinweise


Gibt vollständige Merge‑Feldnamen einschließlich optionalem Präfix zurück. Entfernt keine doppelten Feldnamen.

Wenn das Dokument mehrere Regionen mit demselben Namen enthält, wird die N‑te Region (nullbasiert) verarbeitet.

Bei jedem Aufruf wird ein neues String‑Array erstellt.

## Siehe auch

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
