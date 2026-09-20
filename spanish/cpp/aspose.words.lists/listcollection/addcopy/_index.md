---
title: "Método Aspose::Words::Lists::ListCollection::AddCopy"
linktitle: "AddCopy"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Lists::ListCollection::AddCopy. Crea una nueva lista copiando la lista especificada y añadiéndola a la colección de listas del documento en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.lists/listcollection/addcopy/
---
## ListCollection::AddCopy method


Crea una nueva lista copiando la lista especificada y la agrega a la colección de listas del documento.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddCopy(const System::SharedPtr<Aspose::Words::Lists::List> &srcList)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcList | const System::SharedPtr\<Aspose::Words::Lists::List\>\& | La lista origen de la que copiar. |

### ReturnValue

La lista recién creada.
## Observaciones


La lista origen puede provenir de cualquier documento. Si la lista origen pertenece a un documento diferente, se crea una copia de la lista y se añade al documento actual.

Si la lista origen es una referencia o una definición de un estilo de lista, la lista recién creada no está relacionada con el estilo de lista original.

## Ejemplos



Muestra cómo reiniciar la numeración en una lista copiando una lista.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría.
// Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
// Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// Crea una lista a partir de una plantilla de Microsoft Word y personaliza su primer nivel de lista.
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// Aplica nuestra lista a algunos párrafos.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Podemos agregar una copia de una lista existente a la colección de listas del documento
// para crear una lista similar sin hacer cambios en la original.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// Aplica la segunda lista a nuevos párrafos.
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```

## Ver también

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
