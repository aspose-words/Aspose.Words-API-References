---
title: "Aspose::Words::RevisionGroupCollection::get_Count metodo"
linktitle: "get_Count"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::RevisionGroupCollection::get_Count metodo. Restituisce il numero di gruppi di revisione nella collezione in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/revisiongroupcollection/get_count/
---
## RevisionGroupCollection::get_Count method


Restituisce il numero di gruppi di revisione nella raccolta.

```cpp
int32_t Aspose::Words::RevisionGroupCollection::get_Count()
```


## Esempi



Mostra come stampare le informazioni su un gruppo di revisioni in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

ASSERT_EQ(7, doc->get_Revisions()->get_Groups()->get_Count());

for (auto&& group : doc->get_Revisions()->get_Groups())
{
    std::cout << System::String::Format(u"Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group->get_Author(), group->get_RevisionType(), group->get_Text()) << std::endl;
}
```

## Vedi anche

* Class [RevisionGroupCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
