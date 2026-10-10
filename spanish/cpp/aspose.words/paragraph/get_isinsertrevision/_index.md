---
title: "Aspose::Words::Paragraph::get_IsInsertRevision método"
linktitle: "get_IsInsertRevision"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Paragraph::get_IsInsertRevision método. Devuelve verdadero si este objeto fue insertado en Microsoft Word mientras el seguimiento de cambios estaba habilitado en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words/paragraph/get_isinsertrevision/
---
## Paragraph::get_IsInsertRevision method


Devuelve true si este objeto fue insertado en Microsoft Word mientras el seguimiento de cambios estaba habilitado.

```cpp
bool Aspose::Words::Paragraph::get_IsInsertRevision()
```


## Ejemplos



Muestra cómo trabajar con párrafos de revisión.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();
System::SharedPtr<Aspose::Words::Paragraph> para = body->get_FirstParagraph();

para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Paragraph 1. "));
body->AppendParagraph(u"Paragraph 2. ");
body->AppendParagraph(u"Paragraph 3. ");

// Los párrafos anteriores no son revisiones.
// Los párrafos que añadimos después de iniciar el seguimiento de revisiones se registrarán como revisiones "Insert".
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

para = body->AppendParagraph(u"Paragraph 4. ");

ASSERT_TRUE(para->get_IsInsertRevision());

// Los párrafos que eliminamos después de iniciar el seguimiento de revisiones se registrarán como revisiones "Delete".
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = body->get_Paragraphs();

ASSERT_EQ(4, paragraphs->get_Count());

para = paragraphs->idx_get(2);
para->Remove();

// Estos párrafos permanecerán hasta que aceptemos o rechacemos la revisión de eliminación.
// Aceptar la revisión eliminará el párrafo de forma permanente,
// y rechazar la revisión lo dejará en el documento como si nunca lo hubiéramos eliminado.
ASSERT_EQ(4, paragraphs->get_Count());
ASSERT_TRUE(para->get_IsDeleteRevision());

// Acepta la revisión y luego verifica que el párrafo haya desaparecido.
doc->AcceptAllRevisions();

ASSERT_EQ(3, paragraphs->get_Count());
ASSERT_EQ(0, para->get_Count());
ASSERT_EQ(System::String(u"Paragraph 1. \r") + u"Paragraph 2. \r" + u"Paragraph 4.", doc->GetText().Trim());
```

## Ver también

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
