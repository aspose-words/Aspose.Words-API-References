---
title: "Método Aspose::Words::BookmarkEnd::Accept"
linktitle: "Accept"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::BookmarkEnd::Accept. Acepta un visitante en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/bookmarkend/accept/
---
## BookmarkEnd::Accept method


Acepta un visitante.

```cpp
bool Aspose::Words::BookmarkEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| visitante | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | El visitante que visitará el nodo. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Observaciones


Llama a [VisitBookmarkEnd()](../../documentvisitor/visitbookmarkend/).

Para más información, consulte el patrón de diseño Visitor.

## Ver también

* Class [DocumentVisitor](../../documentvisitor/)
* Class [BookmarkEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
