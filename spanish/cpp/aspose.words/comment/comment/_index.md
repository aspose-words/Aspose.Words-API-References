---
title: "Constructor de Aspose::Words::Comment::Comment"
linktitle: "Comment"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Comment::Comment constructor. Inicializa una nueva instancia de la clase Comment en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/comment/comment/
---
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) constructor


Inicializa una nueva instancia de la clase [Comment](../).

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | El documento propietario. |
## Observaciones


Cuando se crea [Comment](../), pertenece al documento especificado, pero aún no forma parte del documento y [ParentNode](../../node/get_parentnode/) es **null**.

Para agregar [Comment](../) al documento use [InsertAfter1()</see> or <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) en el párrafo donde desea insertar el comentario.

Después de crear un comentario, no olvide establecer sus propiedades [Author](../get_author/), [Initial](../get_initial/) y [DateTime](../get_datetime/).

## Ver también

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) constructor


Inicializa una nueva instancia de la clase [Comment](../).

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, const System::String &author, const System::String &initial, System::DateTime dateTime)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | El documento propietario. |
| autor | const System::String\& | El nombre del autor del comentario. No puede ser **null**. |
| inicial | const System::String\& | Las iniciales del autor del comentario. No pueden ser **null**. |
| dateTime | System::DateTime | La fecha y hora del comentario. |

## Ejemplos



Muestra cómo añadir un comentario a un párrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// En Microsoft Word, podemos hacer clic derecho en este comentario en el cuerpo del documento para editarlo o responderlo.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## Ver también

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
