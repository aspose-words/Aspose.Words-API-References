---
title: "Metodo Aspose::Words::CommentRangeStart::Accept"
linktitle: "Accept"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::CommentRangeStart::Accept. Accetta un visitatore in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/commentrangestart/accept/
---
## CommentRangeStart::Accept method


Accetta un visitatore.

```cpp
bool Aspose::Words::CommentRangeStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitatore | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Il visitatore che visiterà il nodo. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Note


Chiama [VisitCommentRangeStart()](../../documentvisitor/visitcommentrangestart/).

Per ulteriori informazioni vedere il pattern di progettazione Visitor.

## Vedi anche

* Class [DocumentVisitor](../../documentvisitor/)
* Class [CommentRangeStart](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
