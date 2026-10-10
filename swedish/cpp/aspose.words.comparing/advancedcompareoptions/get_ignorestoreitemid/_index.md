---
title: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId metod"
linktitle: "get_IgnoreStoreItemId"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId metod. Anger om skillnad i StructuredDocumentTag lagringsobjekt‑ID ska ignoreras i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.comparing/advancedcompareoptions/get_ignorestoreitemid/
---
## AdvancedCompareOptions::get_IgnoreStoreItemId method


Anger om skillnad i StructuredDocumentTag lagringsobjektets Id ska ignoreras.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId() const
```


## Exempel



Visar hur man jämför SDT med samma innehåll men olika lagringsobjekt-id.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// Konfigurera alternativ för att jämföra SDT med samma innehåll men olika lagringsobjekt-id.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## Se även

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
