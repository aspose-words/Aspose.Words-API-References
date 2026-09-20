---
title: "Clase Aspose::Words::Lists::ListFormat"
linktitle: "ListFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Lists::ListFormat. Permite controlar qué formato de lista se aplica a un párrafo. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.lists/listformat/
---
## ListFormat class


Permite controlar qué formato de lista se aplica a un párrafo. Para obtener más información, visite el artículo de documentación [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListFormat : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [ApplyBulletDefault](./applybulletdefault/)() | Inicia una nueva lista con viñetas predeterminada y la aplica al párrafo. |
| [ApplyNumberDefault](./applynumberdefault/)() | Inicia una nueva lista numerada predeterminada y la aplica al párrafo. |
| [get_IsListItem](./get_islistitem/)() | Verdadero cuando al párrafo se le ha aplicado formato con viñetas o numeración. |
| [get_List](./get_list/)() | Obtiene o establece la lista a la que pertenece este párrafo. |
| [get_ListLevel](./get_listlevel/)() | Devuelve el formato del nivel de lista más cualquier anulación de formato aplicada al párrafo actual. |
| [get_ListLevelNumber](./get_listlevelnumber/)() | Obtiene o establece el número de nivel de lista (0 a 8) para el párrafo. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ListIndent](./listindent/)() | Incrementa el nivel de lista del párrafo actual en un nivel. |
| [ListOutdent](./listoutdent/)() | Disminuye el nivel de lista del párrafo actual en un nivel. |
| [RemoveNumbers](./removenumbers/)() | Elimina los números o viñetas del párrafo actual y establece el nivel de lista a cero. |
| [set_List](./set_list/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Método set para [Aspose::Words::Lists::ListFormat::get_List](./get_list/). |
| [set_ListLevelNumber](./set_listlevelnumber/)(int32_t) | Método set para [Aspose::Words::Lists::ListFormat::get_ListLevelNumber](./get_listlevelnumber/). |
| static [Type](./type/)() |  |
## Observaciones


Un párrafo en un documento de Microsoft Word puede tener viñetas o numeración. Cuando un párrafo tiene viñetas o numeración, se dice que se le ha aplicado formato de lista.

No crea objetos de la clase [ListFormat](./) directamente. Accede a [ListFormat](./) como una propiedad de otro objeto que puede tener formato de lista asociado. En este momento, los objetos que pueden tener formato de lista son: [Paragraph](../../aspose.words/paragraph/), [Style](../../aspose.words/style/) y [DocumentBuilder](../../aspose.words/documentbuilder/).

[ListFormat](./) of a [Paragraph](../../aspose.words/paragraph/) specifies what list formatting and list level is applied to that particular paragraph.

[ListFormat](./) of a [Style](../../aspose.words/style/) (applicable to paragraph styles only) allows to specify what list formatting and list level is applied to all paragraphs of that particular style.

[ListFormat](./) of a [DocumentBuilder](../../aspose.words/documentbuilder/) provides access to the list formatting at the current cursor position inside the [DocumentBuilder](../../aspose.words/documentbuilder/).

El propio formato de lista se almacena dentro de un objeto [List](../list/) que se guarda por separado de los párrafos. Los objetos de lista se almacenan dentro de una colección [ListCollection](../listcollection/). Hay una única colección [ListCollection](../listcollection/) por cada [Document](../../aspose.words/document/).

Los párrafos no pertenecen físicamente a una lista. Los párrafos simplemente hacen referencia a un objeto de lista específico mediante la propiedad [List](./get_list/) y a un nivel particular en la lista mediante la propiedad [ListLevelNumber](./get_listlevelnumber/). Al establecer estas dos propiedades controla qué viñetas y numeración se aplican a un párrafo.

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

## Ver también

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
