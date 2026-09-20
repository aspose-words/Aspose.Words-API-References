---
title: "Aspose::Words::RevisionGroup::get_Text método"
linktitle: "get_Text"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::RevisionGroup::get_Text método. Devuelve el texto insertado/eliminado/movido o una descripción del cambio de formato en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/revisiongroup/get_text/
---
## RevisionGroup::get_Text method


Devuelve el texto insertado/eliminado/movido o la descripción del cambio de formato.

```cpp
System::String Aspose::Words::RevisionGroup::get_Text()
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

* Class [RevisionGroup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
