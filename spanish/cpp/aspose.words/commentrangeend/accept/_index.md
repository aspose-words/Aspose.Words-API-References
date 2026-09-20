---
title: "Método Aspose::Words::CommentRangeEnd::Accept"
linktitle: "Accept"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::CommentRangeEnd::Accept. Acepta un visitante en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/commentrangeend/accept/
---
## CommentRangeEnd::Accept method


Acepta un visitante.

```cpp
bool Aspose::Words::CommentRangeEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| visitante | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | El visitante que visitará el nodo. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Observaciones


Llama a [VisitCommentRangeEnd()](../../documentvisitor/visitcommentrangeend/).

Para más información, consulte el patrón de diseño Visitor.

## Ver también

* Class [DocumentVisitor](../../documentvisitor/)
* Class [CommentRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
