---
title: "Aspose::Words::CommentCollection class"
linktitle: "CommentCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::CommentCollection class. Proporciona acceso tipado a una colección de nodos Comment. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words/commentcollection/
---
## CommentCollection class


Proporciona acceso tipado a una colección de nodos [Comment](../comment/). Para obtener más información, visite el artículo de documentación [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/).

```cpp
class CommentCollection : public Aspose::Words::NodeCollection
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Agrega un nodo al final de la colección. |
| [Clear](../nodecollection/clear/)() | Elimina todos los nodos de esta colección y del documento. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determina si un nodo está en la colección. |
| [get_Count](../nodecollection/get_count/)() | Obtiene el número de nodos en la colección. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Proporciona una iteración simple al estilo "foreach" sobre la colección de nodos. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Recupera un [Comment](../comment/) en el índice dado. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Devuelve el índice basado en cero del nodo especificado. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserta un nodo en la colección en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Elimina el nodo de la colección y del documento. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Elimina el nodo en el índice especificado de la colección y del documento. |
| [ToArray](../nodecollection/toarray/)() | Copia todos los nodos de la colección a una nueva matriz de nodos. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo marcar un comentario como "done".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Helo world!");

// Inserte un comentario para señalar un error.
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Fix the spelling error!");
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Los comentarios tienen una bandera "Done", que se establece en "false" por defecto.
// Si un comentario sugiere que hagamos un cambio dentro del documento,
// podemos aplicar el cambio y luego también establecer la bandera "Done" después para indicar la corrección.
ASSERT_FALSE(comment->get_Done());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Hello world!");
comment->set_Done(true);

// Los comentarios que están "done" se diferenciarán
// de los que no están "hecho" con un color de texto desvanecido.
comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Add text to this paragraph.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.Done.docx");
```

## Ver también

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
