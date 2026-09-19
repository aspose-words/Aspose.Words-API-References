---
title: "Aspose::Words::RevisionGroup::get_RevisionType metodo"
linktitle: "get_RevisionType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::RevisionGroup::get_RevisionType metodo. Ottiene il tipo di revisioni incluse in questo gruppo in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/revisiongroup/get_revisiontype/
---
## RevisionGroup::get_RevisionType method


Ottiene il tipo di revisioni incluse in questo gruppo.

```cpp
Aspose::Words::RevisionType Aspose::Words::RevisionGroup::get_RevisionType()
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

* Enum [RevisionType](../../revisiontype/)
* Class [RevisionGroup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
