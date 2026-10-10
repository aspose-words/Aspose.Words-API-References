---
title: "Aspose::Words::Comment::RemoveReply method"
linktitle: "RemoveReply"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Comment::RemoveReply method. Elimina la respuesta especificada a este comentario en C++."
type: docs
weight: 17000
url: /es/cpp/aspose.words/comment/removereply/
---
## Comment::RemoveReply method


Elimina la respuesta especificada a este comentario.

```cpp
void Aspose::Words::Comment::RemoveReply(const System::SharedPtr<Aspose::Words::Comment> &reply)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| respuesta | const System::SharedPtr\\<Aspose::Words::Comment\\>\\& | El nodo de comentario de la respuesta que se está eliminando. |

## Ejemplos



Muestra cómo eliminar respuestas de comentarios.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"Another reply");

ASSERT_EQ(2, comment->get_Replies()->get_Count());

// A continuación se presentan dos formas de eliminar respuestas de un comentario.
// 1 -  Utilice el método "RemoveReply" para eliminar respuestas de un comentario individualmente:
comment->RemoveReply(comment->get_Replies()->idx_get(0));

ASSERT_EQ(1, comment->get_Replies()->get_Count());

// 2 -  Utilice el método "RemoveAllReplies" para eliminar todas las respuestas de un comentario de una vez:
comment->RemoveAllReplies();

ASSERT_EQ(0, comment->get_Replies()->get_Count());
```

## Ver también

* Class [Comment](../)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
