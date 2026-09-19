---
title: "Aspose::Words::RevisionGroup::get_Text metodo"
linktitle: "get_Text"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::RevisionGroup::get_Text metodo. Restituisce il testo inserito/eliminato/spostato o la descrizione di una modifica di formato in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/revisiongroup/get_text/
---
## RevisionGroup::get_Text method


Restituisce il testo inserito/eliminato/spostato o la descrizione della modifica di formato.

```cpp
System::String Aspose::Words::RevisionGroup::get_Text()
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
