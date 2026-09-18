---
title: "Aspose::Words::Comparing::Granularity Enum"
linktitle: "Granularity"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Comparing::Granularity Enum. Gibt die Granularität der zu verfolgenden Änderungen beim Vergleich von zwei Dokumenten in C++ an."
type: docs
weight: 3000
url: /de/cpp/aspose.words.comparing/granularity/
---
## Granularity enum


Gibt die Granularität der zu verfolgenden Änderungen beim Vergleich von zwei Dokumenten an.

```cpp
enum class Granularity
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| CharLevel | 0 | Gibt Änderungen auf Zeichenebene an. |
| WordLevel | 1 | Gibt Änderungen auf Wortebene an. |


## Beispiele



Zeigt, wie man beim Vergleich von Dokumenten eine Granularität festlegt.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>();
auto builderA = System::MakeObject<Aspose::Words::DocumentBuilder>(docA);
builderA->Writeln(u"Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

auto docB = System::MakeObject<Aspose::Words::Document>();
auto builderB = System::MakeObject<Aspose::Words::DocumentBuilder>(docB);
builderB->Writeln(u"Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Geben Sie an, ob Änderungen verfolgt werden
// nach Zeichen ('Granularity.CharLevel') oder nach Wort ('Granularity.WordLevel').
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_Granularity(granularity);

docA->Compare(docB, u"author", System::DateTime::get_Now(), compareOptions);

// Die Sammlung von Revisionsgruppen des ersten Dokuments enthält alle Unterschiede zwischen den Dokumenten.
System::SharedPtr<Aspose::Words::RevisionGroupCollection> groups = docA->get_Revisions()->get_Groups();
ASSERT_EQ(5, groups->get_Count());
```

## Siehe auch

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
