---
title: "Aspose::Words::Revision::Accept método"
linktitle: "Accept"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Revision::Accept método. Acepta esta revisión en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/revision/accept/
---
## Revision::Accept method


Acepta esta revisión.

```cpp
void Aspose::Words::Revision::Accept()
```


## Ejemplos



Muestra cómo trabajar con revisiones en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// La edición normal del documento no cuenta como una revisión.
builder->Write(u"This does not count as a revision. ");

ASSERT_FALSE(doc->get_HasRevisions());

// Para registrar nuestras ediciones como revisiones, necesitamos declarar un autor y luego comenzar a rastrearlas.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

builder->Write(u"This is revision #1. ");

ASSERT_TRUE(doc->get_HasRevisions());
ASSERT_EQ(1, doc->get_Revisions()->get_Count());

// Esta bandera corresponde a la opción "Review" -> "Tracking" -> "Track Changes" en Microsoft Word.
// El método "StartTrackRevisions" no afecta su valor,
// y el documento está rastreando revisiones programáticamente a pesar de que tiene un valor de "false".
// Si abrimos este documento con Microsoft Word, no estará rastreando revisiones.
ASSERT_FALSE(doc->get_TrackRevisions());

// Hemos añadido texto usando el generador de documentos, por lo que la primera revisión es una revisión de tipo inserción.
System::SharedPtr<Aspose::Words::Revision> revision = doc->get_Revisions()->idx_get(0);
ASSERT_EQ(u"John Doe", revision->get_Author());
ASSERT_EQ(u"This is revision #1. ", revision->get_ParentNode()->GetText());
ASSERT_EQ(Aspose::Words::RevisionType::Insertion, revision->get_RevisionType());
ASSERT_EQ(revision->get_DateTime().get_Date(), System::DateTime::get_Now().get_Date());
ASPOSE_ASSERT_EQ(doc->get_Revisions()->get_Groups()->idx_get(0), revision->get_Group());

// Elimine un run para crear una revisión de tipo eliminación.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->Remove();

// Agregar una nueva revisión la coloca al principio de la colección de revisiones.
ASSERT_EQ(Aspose::Words::RevisionType::Deletion, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(2, doc->get_Revisions()->get_Count());

// Las revisiones de inserción aparecen en el cuerpo del documento incluso antes de aceptar/rechazar la revisión.
// Rechazar la revisión eliminará sus nodos del cuerpo. Por el contrario, los nodos que componen revisiones de eliminación
// también permanecen en el documento hasta que aceptemos la revisión.
ASSERT_EQ(u"This does not count as a revision. This is revision #1.", doc->GetText().Trim());

// Aceptar la revisión de eliminación eliminará su nodo padre del texto del párrafo
// y luego eliminará la propia revisión de la colección.
doc->get_Revisions()->idx_get(0)->Accept();

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1.", doc->GetText().Trim());

builder->Writeln(u"");
builder->Write(u"This is revision #2.");

// Ahora mueva el nodo para crear un tipo de revisión de movimiento.
System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1);
System::SharedPtr<Aspose::Words::Node> endNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_NextSibling();
System::SharedPtr<Aspose::Words::Node> referenceNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0);

while (node != endNode)
{
    System::SharedPtr<Aspose::Words::Node> nextNode = node->get_NextSibling();
    doc->get_FirstSection()->get_Body()->InsertBefore<System::SharedPtr<Aspose::Words::Node>>(node, referenceNode);
    node = nextNode;
}

ASSERT_EQ(Aspose::Words::RevisionType::Moving, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(8, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc->GetText().Trim());

// La revisión de movimiento está ahora en el índice 1. Rechace la revisión para descartar su contenido.
doc->get_Revisions()->idx_get(1)->Reject();

ASSERT_EQ(6, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1. \rThis is revision #2.", doc->GetText().Trim());
```

## Ver también

* Class [Revision](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
