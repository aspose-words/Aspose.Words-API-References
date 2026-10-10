---
title: "Aspose::Words::RevisionGroup class"
linktitle: "RevisionGroup"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::RevisionGroup class. Representa un grupo de objetos Revision secuenciales. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 54000
url: /es/cpp/aspose.words/revisiongroup/
---
## RevisionGroup class


Representa un grupo de objetos [Revision](../revision/) secuenciales. Para obtener más información, visite el artículo de documentación [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/).

```cpp
class RevisionGroup : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Author](./get_author/)() | Obtiene el autor de este grupo de revisiones. |
| [get_RevisionType](./get_revisiontype/)() | Obtiene el tipo de revisiones incluidas en este grupo. |
| [get_Text](./get_text/)() | Devuelve el texto insertado/eliminado/movido o la descripción del cambio de formato. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
