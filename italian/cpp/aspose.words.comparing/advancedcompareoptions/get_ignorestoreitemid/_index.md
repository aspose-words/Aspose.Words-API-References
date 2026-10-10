---
title: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId metodo"
linktitle: "get_IgnoreStoreItemId"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId metodo. Specifica se ignorare la differenza nell'Id dell'elemento di archiviazione StructuredDocumentTag in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.comparing/advancedcompareoptions/get_ignorestoreitemid/
---
## AdvancedCompareOptions::get_IgnoreStoreItemId method


Specifica se ignorare le differenze nell'Id dell'elemento di archiviazione StructuredDocumentTag.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId() const
```


## Esempi



Mostra come confrontare SDT con lo stesso contenuto ma con un id dell'elemento di archiviazione diverso.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// Configura le opzioni per confrontare SDT con lo stesso contenuto ma con un id dell'elemento di archiviazione diverso.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## Vedi anche

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
