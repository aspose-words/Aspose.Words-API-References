---
title: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId Methode"
linktitle: "get_IgnoreDmlUniqueId"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId Methode. Gibt an, ob Unterschiede in der eindeutigen DrawingML unique Id in C++ ignoriert werden sollen."
type: docs
weight: 3000
url: /de/cpp/aspose.words.comparing/advancedcompareoptions/get_ignoredmluniqueid/
---
## AdvancedCompareOptions::get_IgnoreDmlUniqueId method


Gibt an, ob Unterschiede in der eindeutigen DrawingML‑Id ignoriert werden sollen.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId() const
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

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
