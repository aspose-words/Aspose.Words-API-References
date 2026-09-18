---
title: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId-Methode"
linktitle: "get_IgnoreStoreItemId"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId-Methode. Gibt an, ob Unterschiede in der Store-Item-ID des StructuredDocumentTag in C++ ignoriert werden sollen."
type: docs
weight: 4000
url: /de/cpp/aspose.words.comparing/advancedcompareoptions/get_ignorestoreitemid/
---
## AdvancedCompareOptions::get_IgnoreStoreItemId method


Gibt an, ob Unterschiede in der Store‑Item‑Id des StructuredDocumentTag ignoriert werden sollen.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId() const
```


## Beispiele



Zeigt, wie man SDT mit gleichem Inhalt, aber unterschiedlicher Store‑Item‑Id vergleicht.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// Konfigurieren Sie Optionen, um SDT mit gleichem Inhalt, aber unterschiedlicher Store‑Item‑Id zu vergleichen.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## Siehe auch

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
