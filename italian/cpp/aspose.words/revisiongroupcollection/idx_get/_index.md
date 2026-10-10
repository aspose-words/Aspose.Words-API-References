---
title: "Aspose::Words::RevisionGroupCollection::idx_get metodo"
linktitle: "idx_get"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::RevisionGroupCollection::idx_get metodo. Restituisce un gruppo di revisioni all'indice specificato in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words/revisiongroupcollection/idx_get/
---
## RevisionGroupCollection::idx_get method


Restituisce un gruppo di revisione all'indice specificato.

```cpp
System::SharedPtr<Aspose::Words::RevisionGroup> Aspose::Words::RevisionGroupCollection::idx_get(int32_t index)
```


## Esempi



Mostra come ottenere un gruppo di revisioni in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::RevisionGroup> revisionGroup = doc->get_Revisions()->get_Groups()->idx_get(0);
```

## Vedi anche

* Class [RevisionGroup](../../revisiongroup/)
* Class [RevisionGroupCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
