---
title: "Aspose::Words::Comment::SetText método"
linktitle: "SetText"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Comment::SetText method. Este es un método de conveniencia que permite establecer fácilmente el texto del comentario en C++."
type: docs
weight: 22000
url: /es/cpp/aspose.words/comment/settext/
---
## Comment::SetText method


Este es un método de conveniencia que permite establecer fácilmente el texto del comentario.

```cpp
void Aspose::Words::Comment::SetText(const System::String &text)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| texto | const System::String\& | El nuevo texto del comentario. |
## Observaciones


Este método permite establecer rápidamente el texto de un comentario a partir de una cadena. La cadena puede contener saltos de párrafo, lo que creará párrafos de texto en el comentario de forma correspondiente. Si desea insertar elementos más complejos en el comentario, por ejemplo marcadores o tablas o aplicar formato enriquecido, entonces necesita usar las clases de nodo apropiadas para construir el texto del comentario.

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
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
