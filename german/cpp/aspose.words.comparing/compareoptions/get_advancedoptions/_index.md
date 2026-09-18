---
title: "Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions Methode"
linktitle: "get_AdvancedOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions Methode. Gibt erweiterte Vergleichsoptionen an, die dabei helfen können, genauere Vergleichsergebnisse in C++ zu erzeugen."
type: docs
weight: 2500
url: /de/cpp/aspose.words.comparing/compareoptions/get_advancedoptions/
---
## CompareOptions::get_AdvancedOptions method


Gibt erweiterte Vergleichsoptionen an, die dabei helfen können, ein präziseres Vergleichsergebnis zu erzeugen.

```cpp
const System::SharedPtr<Aspose::Words::Comparing::AdvancedCompareOptions> & Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions() const
```


## Beispiele



Zeigt, wie Dokumente verglichen werden, wobei die eindeutige DML‑ID ignoriert wird.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID original.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID compare.docx");

// Standardmäßig ignoriert Aspose.Words die eindeutige DML‑ID nicht, und die Anzahl der Revisionen betrug 2.
// Wenn wir die eindeutige DML‑ID ignorieren, beträgt die Anzahl der Revisionen 0.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreDmlUniqueId(isIgnoreDmlUniqueId);

docA->Compare(docB, u"Aspose.Words", System::DateTime::get_Now(), compareOptions);

ASSERT_EQ(isIgnoreDmlUniqueId ? 0 : 2, docA->get_Revisions()->get_Count());
```

## Siehe auch

* Class [AdvancedCompareOptions](../../advancedcompareoptions/)
* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
