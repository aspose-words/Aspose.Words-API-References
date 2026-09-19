---
title: "Aspose::Words::BookmarkStart::Accept metodo"
linktitle: "Accept"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BookmarkStart::Accept metodo. Accetta un visitatore in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/bookmarkstart/accept/
---
## BookmarkStart::Accept method


Accetta un visitatore.

```cpp
bool Aspose::Words::BookmarkStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitatore | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Il visitatore che visiterà il nodo. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Note


Chiama [VisitBookmarkStart()](../../documentvisitor/visitbookmarkstart/).

Per ulteriori informazioni vedere il pattern di progettazione Visitor.

## Vedi anche

* Class [DocumentVisitor](../../documentvisitor/)
* Class [BookmarkStart](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
