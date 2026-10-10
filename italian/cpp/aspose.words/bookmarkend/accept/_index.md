---
title: "Aspose::Words::BookmarkEnd::Accept metodo"
linktitle: "Accept"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BookmarkEnd::Accept metodo. Accetta un visitatore in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/bookmarkend/accept/
---
## BookmarkEnd::Accept method


Accetta un visitatore.

```cpp
bool Aspose::Words::BookmarkEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitatore | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Il visitatore che visiterà il nodo. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Note


Chiama [VisitBookmarkEnd()](../../documentvisitor/visitbookmarkend/).

Per ulteriori informazioni vedere il pattern di progettazione Visitor.

## Vedi anche

* Class [DocumentVisitor](../../documentvisitor/)
* Class [BookmarkEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
