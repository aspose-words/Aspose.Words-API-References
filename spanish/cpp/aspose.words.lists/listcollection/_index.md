---
title: "Aspose::Words::Lists::ListCollection class"
linktitle: "ListCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Lists::ListCollection class. Almacena y gestiona el formato de listas con viñetas y numeradas usadas en un documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.lists/listcollection/
---
## ListCollection class


Almacena y gestiona el formato de listas con viñetas y numeradas usadas en un documento. Para obtener más información, visite el artículo de documentación [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Lists::List>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](./add/)(Aspose::Words::Lists::ListTemplate) | Crea una nueva lista basada en una plantilla predefinida y la agrega a la colección de listas del documento. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Crea una nueva lista que hace referencia a un estilo de lista y la agrega a la colección de listas del documento. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Crea una nueva lista copiando la lista especificada y la agrega a la colección de listas del documento. |
| [AddSingleLevelList](./addsinglelevellist/)(Aspose::Words::Lists::ListTemplate) | Crea una nueva lista de un solo nivel basada en la plantilla predefinida y la agrega a la colección de listas del documento. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtiene el recuento de listas numeradas y con viñetas en el documento. |
| [get_Document](./get_document/)() const | Obtiene el documento propietario. |
| [GetEnumerator](./getenumerator/)() override | Obtiene el objeto enumerador que enumerará las listas en el documento. |
| [GetListByListId](./getlistbylistid/)(int32_t) | Obtiene una lista por un identificador de lista. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Obtiene una lista por índice. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Descripción |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Observaciones


Una lista en un documento de Microsoft Word es un conjunto de propiedades de formato de lista. El formato de las listas se almacena en la colección [ListCollection](./) por separado de los párrafos de texto.

No crea objetos de esta clase. Siempre hay un solo objeto [ListCollection](./) por documento y es accesible a través de la propiedad [Lists](../../aspose.words/documentbase/get_lists/).

Para crear una nueva lista basada en una plantilla de lista predefinida o en un estilo de lista, use el método [Add()](../).

Para crear una nueva lista con un formato idéntico a una lista existente, use el método [AddCopy()](../).

Para que un párrafo tenga viñetas o numeración, debe aplicar formato de lista a un párrafo asignando un objeto [List](../list/) a la propiedad [List](../listformat/get_list/) de [ListFormat](../listformat/).

Para eliminar el formato de lista de un párrafo, use el método [RemoveNumbers](../listformat/removenumbers/).

Si conoce un poco sobre WordprocessingML, entonces sabrá que define conceptos separados para "list" y "list definition". Esto corresponde exactamente a cómo se almacena el formato de lista en un documento de Microsoft Word a bajo nivel. La definición de [List](../list/) es como un "esquema" y la lista es como una instancia de una definición de lista.

Para simplificar el modelo de programación, Aspose.Words oculta la distinción entre lista y definición de lista de manera similar a como Microsoft Word lo oculta en su interfaz de usuario. Esto le permite concentrarse más en cómo desea que se vea su documento, en lugar de construir objetos de bajo nivel para cumplir con los requisitos del formato de archivo de Microsoft Word.

No es posible eliminar listas una vez que se crean en la versión actual de [Aspose.Words](../../aspose.words/). Esto es similar a Microsoft Word, donde el usuario no tiene control explícito sobre las definiciones de lista.

## Ejemplos



Muestra cómo trabajar con niveles de lista.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría.
// Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
// Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// A continuación se presentan dos tipos de listas que podemos crear usando un document builder.
// 1 -  Una lista numerada:
// Las listas numeradas crean un orden lógico para sus párrafos numerando cada elemento.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// Al establecer la propiedad "ListLevelNumber", podemos aumentar el nivel de la lista
// para iniciar una sublista autocontenida en el elemento de lista actual.
// La plantilla de lista de Microsoft Word llamada "NumberDefault" usa números para crear niveles de lista para el primer nivel de lista.
// Los niveles de lista más profundos usan letras y números romanos en minúscula.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  Una lista con viñetas:
// Esta lista aplicará una sangría y un símbolo de viñeta ("•") antes de cada párrafo.
// Los niveles más profundos de esta lista usarán símbolos diferentes, como "■" y "○".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// Podemos desactivar el formato de lista para que no formatee los párrafos subsecuentes como listas desactivando la bandera "List".
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```


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

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
