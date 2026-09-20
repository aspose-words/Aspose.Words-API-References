---
title: "Método Aspose::Words::RevisionGroupCollection::get_Count"
linktitle: "get_Count"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::RevisionGroupCollection::get_Count. Devuelve el número de grupos de revisión en la colección en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/revisiongroupcollection/get_count/
---
## RevisionGroupCollection::get_Count method


Devuelve el número de grupos de revisiones en la colección.

```cpp
int32_t Aspose::Words::RevisionGroupCollection::get_Count()
```


## Ejemplos



Muestra cómo imprimir información sobre un grupo de revisiones en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

ASSERT_EQ(7, doc->get_Revisions()->get_Groups()->get_Count());

for (auto&& group : doc->get_Revisions()->get_Groups())
{
    std::cout << System::String::Format(u"Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group->get_Author(), group->get_RevisionType(), group->get_Text()) << std::endl;
}
```

## Ver también

* Class [RevisionGroupCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
