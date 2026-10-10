---
title: "Aspose::Words::RevisionGroup::get_Author metodo"
linktitle: "get_Author"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::RevisionGroup::get_Author metodo. Ottiene l'autore di questo gruppo di revisioni in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/revisiongroup/get_author/
---
## RevisionGroup::get_Author method


Ottiene l'autore di questo gruppo di revisioni.

```cpp
System::String Aspose::Words::RevisionGroup::get_Author()
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

* Class [RevisionGroup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
