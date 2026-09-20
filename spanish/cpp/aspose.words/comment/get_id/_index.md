---
title: "Aspose::Words::Comment::get_Id método"
linktitle: "get_Id"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Comment::get_Id método. Obtiene o establece el identificador del comentario en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words/comment/get_id/
---
## Comment::get_Id method


Obtiene o establece el identificador del comentario.

```cpp
int32_t Aspose::Words::Comment::get_Id() const
```

## Observaciones


El identificador del comentario permite anclar un comentario a una región de texto en el documento. La región debe estar delimitada usando los objetos [CommentRangeStart](../../commentrangestart/) y [CommentRangeEnd](../../commentrangeend/) que comparten el mismo valor de identificador que el objeto [Comment](../).

Usaría este valor al buscar los nodos [CommentRangeStart](../../commentrangestart/) y [CommentRangeEnd](../../commentrangeend/) que están vinculados a este comentario.

[Comment](../) identifiers are supposed to be unique across a document and Aspose.Words automatically maintains comment identifiers when loading, saving and combining documents. 
## Ver también

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
