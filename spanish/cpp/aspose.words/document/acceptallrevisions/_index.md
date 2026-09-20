---
title: "Aspose::Words::Document::AcceptAllRevisions método"
linktitle: "AcceptAllRevisions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::AcceptAllRevisions método. Acepta todos los cambios rastreados en el documento en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/document/acceptallrevisions/
---
## Document::AcceptAllRevisions method


Acepta todos los cambios controlados en el documento.

```cpp
void Aspose::Words::Document::AcceptAllRevisions()
```


## Ejemplos



Muestra cómo aceptar todos los cambios de seguimiento en el documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Edita el documento mientras rastreas cambios para crear algunas revisiones.
doc->StartTrackRevisions(u"John Doe");
builder->Write(u"Hello world! ");
builder->Write(u"Hello again! ");
builder->Write(u"This is another revision.");
doc->StopTrackRevisions();

ASSERT_EQ(3, doc->get_Revisions()->get_Count());

// Podemos iterar a través de cada revisión y aceptarla/rechazarla como parte de nuestro documento.
// Si sabemos que deseamos aceptar cada revisión, podemos hacerlo de manera más directa llamando a este método.
doc->AcceptAllRevisions();

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"Hello world! Hello again! This is another revision.", doc->GetText().Trim());
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
