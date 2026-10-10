---
title: "Aspose::Words::CommentRangeEnd::Accept metodo"
linktitle: "Accept"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::CommentRangeEnd::Accept metodo. Accetta un visitatore in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/commentrangeend/accept/
---
## CommentRangeEnd::Accept method


Accetta un visitatore.

```cpp
bool Aspose::Words::CommentRangeEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitatore | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Il visitatore che visiterà il nodo. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Note


Chiama [VisitCommentRangeEnd()](../../documentvisitor/visitcommentrangeend/).

Per ulteriori informazioni vedere il pattern di progettazione Visitor.

## Vedi anche

* Class [DocumentVisitor](../../documentvisitor/)
* Class [CommentRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
