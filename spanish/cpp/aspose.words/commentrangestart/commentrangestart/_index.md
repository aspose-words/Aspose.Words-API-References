---
title: "Constructor Aspose::Words::CommentRangeStart::CommentRangeStart"
linktitle: "CommentRangeStart"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Constructor Aspose::Words::CommentRangeStart::CommentRangeStart. Inicializa una nueva instancia de esta clase en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/commentrangestart/commentrangestart/
---
## CommentRangeStart::CommentRangeStart constructor


Inicializa una nueva instancia de esta clase.

```cpp
Aspose::Words::CommentRangeStart::CommentRangeStart(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, int32_t id)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | El documento propietario. |
| id | int32_t | El identificador del comentario al que está vinculado este objeto. |
## Observaciones


Cuando se crea [CommentRangeStart](../), pertenece al documento especificado, pero aún no forma parte del documento y [ParentNode](../../node/get_parentnode/) es **null**.

Para agregar un [CommentRangeStart](../) al documento, use InsertAfter o InsertBefore en el párrafo donde desea insertar el comentario.

## Ver también

* Class [DocumentBase](../../documentbase/)
* Class [CommentRangeStart](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
