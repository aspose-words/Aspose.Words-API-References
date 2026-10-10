---
title: "Aspose::Words::Comment::get_Author método"
linktitle: "get_Author"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Comment::get_Author método. Devuelve o establece el nombre del autor de un comentario en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/comment/get_author/
---
## Comment::get_Author method


Obtiene o establece el nombre del autor de un comentario.

```cpp
System::String Aspose::Words::Comment::get_Author() const
```

## Observaciones


No puede ser **null**.

El valor predeterminado es una cadena vacía.

## Ejemplos



Muestra cómo imprimir todos los comentarios de un documento y sus respuestas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Comments.docx");

System::SharedPtr<Aspose::Words::NodeCollection> comments = doc->GetChildNodes(Aspose::Words::NodeType::Comment, true);

// Si un comentario no tiene ancestro, es un comentario de "nivel superior" en contraposición a un comentario de tipo respuesta.
// Imprime todos los comentarios de nivel superior junto con cualquier respuesta que puedan tener.
for (auto&& comment : comments->LINQ_OfType<System::SharedPtr<Aspose::Words::Comment> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Comment>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Comment> c)>>([](System::SharedPtr<Aspose::Words::Comment> c) -> bool
{
    return c->get_Ancestor() == nullptr;
})))->LINQ_ToList())
{
    std::cout << "Top-level comment:" << std::endl;
    std::cout << System::String::Format(u"\t\"{0}\", by {1}", comment->GetText().Trim(), comment->get_Author()) << std::endl;
    std::cout << System::String::Format(u"Has {0} replies", comment->get_Replies()->get_Count()) << std::endl;
    for (auto&& commentReply : System::IterateOver<Aspose::Words::Comment>(comment->get_Replies()))
    {
        std::cout << System::String::Format(u"\t\"{0}\", by {1}", commentReply->GetText().Trim(), commentReply->get_Author()) << std::endl;
    }
    std::cout << std::endl;
}
```

## Ver también

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
