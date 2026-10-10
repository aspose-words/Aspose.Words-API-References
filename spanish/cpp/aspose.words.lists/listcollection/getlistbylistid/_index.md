---
title: "Aspose::Words::Lists::ListCollection::GetListByListId method"
linktitle: "GetListByListId"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Lists::ListCollection::GetListByListId method. Obtiene una lista mediante un identificador de lista en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection::GetListByListId method


Obtiene una lista por un identificador de lista.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::GetListByListId(int32_t listId)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| listId | int32_t | El identificador de la lista. |

### ReturnValue

Devuelve el objeto lista. Devuelve **null** si no se encontró una lista con el identificador especificado.
## Observaciones


Normalmente no necesitas usar este método. La mayoría de las veces aplicas el formato de lista a los párrafos simplemente configurando la propiedad [List](../../listformat/get_list/) del objeto [ListFormat](../../listformat/).

## Ejemplos



Muestra cómo verificar las propiedades del documento propietario de las listas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Lists::ListCollection> lists = doc->get_Lists();
ASPOSE_ASSERT_EQ(doc, lists->get_Document());

System::SharedPtr<Aspose::Words::Lists::List> list = lists->Add(Aspose::Words::Lists::ListTemplate::BulletDefault);
ASPOSE_ASSERT_EQ(doc, list->get_Document());

std::cout << (System::String(u"Current list count: ") + lists->get_Count()) << std::endl;
std::cout << (System::String(u"Is the first document list: ") + (System::ObjectExt::Equals(lists->idx_get(0), list))) << std::endl;
std::cout << (System::String(u"ListId: ") + list->get_ListId()) << std::endl;
std::cout << (System::String(u"List is the same by ListId: ") + (System::ObjectExt::Equals(lists->GetListByListId(1), list))) << std::endl;
```

## Ver también

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
