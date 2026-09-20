---
title: "Método Aspose::Words::Comment::AddReply"
linktitle: "AddReply"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Comment::AddReply. Añade una respuesta a este comentario en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/comment/addreply/
---
## Comment::AddReply method


Agrega una respuesta a este comentario.

```cpp
System::SharedPtr<Aspose::Words::Comment> Aspose::Words::Comment::AddReply(const System::String &author, const System::String &initial, System::DateTime dateTime, const System::String &text)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| autor | const System::String\& | El nombre del autor de la respuesta. |
| inicial | const System::String\& | Las iniciales del autor de la respuesta. |
| dateTime | System::DateTime | La fecha y hora de la respuesta. |
| texto | const System::String\& | El texto de la respuesta. |

### ReturnValue

El nodo [Comment](../) creado para la respuesta.
## Observaciones


Debido a las limitaciones existentes de MS Office, solo se permite 1 nivel de respuestas en el documento.

## Ejemplos



Muestra cómo agregar un comentario a un documento y luego responder a él.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// Coloque el comentario en un nodo del cuerpo del documento.
// Este comentario aparecerá en la ubicación de su párrafo,
// fuera del margen derecho de la página, y con una línea punteada que lo conecta a su párrafo.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Agregue una respuesta, que aparecerá bajo su comentario padre.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// Los comentarios y las respuestas son ambos nodos Comment.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// Los comentarios que no responden a otros comentarios son "de nivel superior". No tienen comentarios ancestros.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// Las respuestas tienen un comentario ancestro de nivel superior.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```

## Ver también

* Class [Comment](../)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
