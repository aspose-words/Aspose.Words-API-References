---
title: "Metodo Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions"
linktitle: "get_AdvancedOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions. Specifica opzioni avanzate di confronto che potrebbero aiutare a produrre un output di confronto più preciso in C++."
type: docs
weight: 2500
url: /it/cpp/aspose.words.comparing/compareoptions/get_advancedoptions/
---
## CompareOptions::get_AdvancedOptions method


Specifica opzioni di confronto avanzate che potrebbero aiutare a produrre un output di confronto più preciso.

```cpp
const System::SharedPtr<Aspose::Words::Comparing::AdvancedCompareOptions> & Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions() const
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

* Class [AdvancedCompareOptions](../../advancedcompareoptions/)
* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
