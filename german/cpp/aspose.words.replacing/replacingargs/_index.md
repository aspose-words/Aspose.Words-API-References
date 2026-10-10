---
title: "Aspose::Words::Replacing::ReplacingArgs Klasse"
linktitle: "ReplacingArgs"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Replacing::ReplacingArgs Klasse. Stellt Daten für eine benutzerdefinierte Ersetzungsoperation bereit. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.replacing/replacingargs/
---
## ReplacingArgs class


Stellt Daten für eine benutzerdefinierte Ersetzen-Operation bereit. Weitere Informationen finden Sie im [Find and Replace](https://docs.aspose.com/words/cpp/find-and-replace/) Dokumentationsartikel.

```cpp
class ReplacingArgs : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_GroupIndex](./get_groupindex/)() const | Identifiziert, nach Index, eine erfasste Gruppe im [Match](./get_match/), die durch die [Replacement](./get_replacement/)-Zeichenkette ersetzt werden soll. |
| [get_GroupName](./get_groupname/)() const | Identifiziert, nach Name, eine erfasste Gruppe im [Match](./get_match/), die durch die [Replacement](./get_replacement/)-Zeichenkette ersetzt werden soll. |
| [get_Match](./get_match/)() const | Das **Match**, das aus einem einzelnen regulären Ausdrucks‑Match während eines **Replace** resultiert. |
| [get_MatchEndNode](./get_matchendnode/)() const | Gibt den Knoten zurück, der das Ende des Matches enthält. |
| [get_MatchNode](./get_matchnode/)() const | Gibt den Knoten zurück, der den Anfang des Matches enthält. |
| [get_MatchOffset](./get_matchoffset/)() const | Gibt die nullbasierte Startposition des Matches ab dem Beginn des Knotens zurück, der den Anfang des Matches enthält. |
| [get_Replacement](./get_replacement/)() const | Gibt die Ersetzungszeichenkette zurück. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_GroupIndex](./set_groupindex/)(int32_t) | Setter für [Aspose::Words::Replacing::ReplacingArgs::get_GroupIndex](./get_groupindex/). |
| [set_GroupName](./set_groupname/)(const System::String\&) | Setter für [Aspose::Words::Replacing::ReplacingArgs::get_GroupName](./get_groupname/). |
| [set_Replacement](./set_replacement/)(const System::String\&) | Setzt die Ersetzungszeichenkette. |
| static [Type](./type/)() |  |

## Siehe auch

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
