---
title: "Aspose::Words::WarningInfoCollection::idx_get metodo"
linktitle: "idx_get"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::WarningInfoCollection::idx_get metodo. Ottiene un elemento all'indice specificato in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words/warninginfocollection/idx_get/
---
## WarningInfoCollection::idx_get method


Ottiene un elemento all'indice specificato.

```cpp
System::SharedPtr<Aspose::Words::WarningInfo> Aspose::Words::WarningInfoCollection::idx_get(int32_t index)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | Indice basato su zero dell'elemento. |

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

* Class [WarningInfo](../../warninginfo/)
* Class [WarningInfoCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
