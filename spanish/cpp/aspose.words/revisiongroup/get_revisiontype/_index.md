---
title: "Aspose::Words::RevisionGroup::get_RevisionType método"
linktitle: "get_RevisionType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::RevisionGroup::get_RevisionType método. Obtiene el tipo de revisiones incluidas en este grupo en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/revisiongroup/get_revisiontype/
---
## RevisionGroup::get_RevisionType method


Obtiene el tipo de revisiones incluidas en este grupo.

```cpp
Aspose::Words::RevisionType Aspose::Words::RevisionGroup::get_RevisionType()
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

* Enum [RevisionType](../../revisiontype/)
* Class [RevisionGroup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
