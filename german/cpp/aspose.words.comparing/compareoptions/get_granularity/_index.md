---
title: "Aspose::Words::Comparing::CompareOptions::get_Granularity Methode"
linktitle: "get_Granularity"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Comparing::CompareOptions::get_Granularity Methode. Gibt an, ob Änderungen Zeichenweise oder wortweise in C++ nachverfolgt werden."
type: docs
weight: 4000
url: /de/cpp/aspose.words.comparing/compareoptions/get_granularity/
---
## CompareOptions::get_Granularity method


Gibt an, ob Änderungen Zeichenweise oder wortweise nachverfolgt werden.

```cpp
Aspose::Words::Comparing::Granularity Aspose::Words::Comparing::CompareOptions::get_Granularity() const
```


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

* Enum [Granularity](../../granularity/)
* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
