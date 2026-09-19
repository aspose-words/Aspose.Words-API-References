---
title: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId metodo"
linktitle: "get_IgnoreDmlUniqueId"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId metodo. Specifica se ignorare la differenza nell'ID univoco di DrawingML in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.comparing/advancedcompareoptions/get_ignoredmluniqueid/
---
## AdvancedCompareOptions::get_IgnoreDmlUniqueId method


Specifica se ignorare le differenze nell'Id univoco di DrawingML.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId() const
```


## Esempi



Mostra come confrontare i documenti ignorando l'ID univoco DML.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID original.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID compare.docx");

// Per impostazione predefinita, Aspose.Words non ignora l'ID univoco di DML e il conteggio delle revisioni era 2.
// Se ignoriamo l'ID univoco di DML, il conteggio delle revisioni è 0.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreDmlUniqueId(isIgnoreDmlUniqueId);

docA->Compare(docB, u"Aspose.Words", System::DateTime::get_Now(), compareOptions);

ASSERT_EQ(isIgnoreDmlUniqueId ? 0 : 2, docA->get_Revisions()->get_Count());
```

## Vedi anche

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
