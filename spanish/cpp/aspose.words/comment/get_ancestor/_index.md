---
title: "Aspose::Words::Comment::get_Ancestor método"
linktitle: "get_Ancestor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Comment::get_Ancestor método. Devuelve el objeto Comment padre. Devuelve null para los comentarios de nivel superior en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/comment/get_ancestor/
---
## Comment::get_Ancestor method


Devuelve el objeto [Comment](../) padre. Devuelve **null** para los comentarios de nivel superior.

```cpp
System::SharedPtr<Aspose::Words::Comment> Aspose::Words::Comment::get_Ancestor()
```


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
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
