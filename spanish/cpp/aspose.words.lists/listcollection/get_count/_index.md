---
title: "Aspose::Words::Lists::ListCollection::get_Count method"
linktitle: "get_Count"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Lists::ListCollection::get_Count method. Obtiene el recuento de listas numeradas y con viñetas en el documento en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.lists/listcollection/get_count/
---
## ListCollection::get_Count method


Obtiene el recuento de listas numeradas y con viñetas en el documento.

```cpp
int32_t Aspose::Words::Lists::ListCollection::get_Count()
```


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

* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
