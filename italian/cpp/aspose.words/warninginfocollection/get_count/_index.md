---
title: "Aspose::Words::WarningInfoCollection::get_Count metodo"
linktitle: "get_Count"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::WarningInfoCollection::get_Count metodo. Ottiene il numero di elementi contenuti nella collezione in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words/warninginfocollection/get_count/
---
## WarningInfoCollection::get_Count method


Ottiene il numero di elementi contenuti nella raccolta.

```cpp
int32_t Aspose::Words::WarningInfoCollection::get_Count()
```


## Esempi



Mostra come ottenere avvisi su formati non supportati.
```cpp
auto warnings = System::MakeObject<Aspose::Words::WarningInfoCollection>();
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_WarningCallback(warnings);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"FB2 document.fb2", loadOptions);

ASSERT_EQ(u"The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings->idx_get(0)->get_Description());
ASSERT_EQ(1, warnings->get_Count());
```

## Vedi anche

* Class [WarningInfoCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
