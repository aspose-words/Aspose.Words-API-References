---
title: "Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion metod"
linktitle: "GetFieldNamesForRegion"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion metod. Returnerar en samling av mail merge-fältnamn som är tillgängliga i regionen i C++."
type: docs
weight: 22000
url: /sv/cpp/aspose.words.mailmerging/mailmerge/getfieldnamesforregion/
---
## MailMerge::GetFieldNamesForRegion(const System::String\&) method


Returnerar en samling av mail merge‑fältnamn som finns i regionen.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| regionName | const System::String\& | Regionnamn (skiftlägesokänslig). |
## Anmärkningar


Returnerar fullständiga postfusionsfältnamn inklusive valfritt prefix. Eliminera inte dubblettfältnamn.

Om dokumentet innehåller flera regioner med samma namn bearbetas den allra första regionen.

En ny strängarray skapas vid varje anrop.

## Se även

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::GetFieldNamesForRegion(const System::String\&, int32_t) method


Returnerar en samling av mail merge‑fältnamn som finns i regionen.

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName, int32_t regionIndex)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| regionName | const System::String\& | Regionnamn (skiftlägesokänslig). |
| regionIndex | int32_t | Regionindex (nollbaserat). |
## Anmärkningar


Returnerar fullständiga postfusionsfältnamn inklusive valfritt prefix. Eliminera inte dubblettfältnamn.

Om dokumentet innehåller flera regioner med samma namn bearbetas den N:e regionen (nollbaserat).

En ny strängarray skapas vid varje anrop.

## Se även

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
