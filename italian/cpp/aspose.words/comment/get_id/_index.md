---
title: "Aspose::Words::Comment::get_Id method"
linktitle: "get_Id"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Comment::get_Id method. Ottiene o imposta l'identificatore del commento in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words/comment/get_id/
---
## Comment::get_Id method


Ottiene o imposta l'identificatore del commento.

```cpp
int32_t Aspose::Words::Comment::get_Id() const
```

## Note


L'identificatore del commento consente di ancorare un commento a una regione di testo nel documento. La regione deve essere delimitata utilizzando gli oggetti [CommentRangeStart](../../commentrangestart/) e [CommentRangeEnd](../../commentrangeend/) che condividono lo stesso valore di identificatore dell'oggetto [Comment](../).

Si utilizza questo valore quando si cercano i nodi [CommentRangeStart](../../commentrangestart/) e [CommentRangeEnd](../../commentrangeend/) collegati a questo commento.

[Comment](../) identifiers are supposed to be unique across a document and Aspose.Words automatically maintains comment identifiers when loading, saving and combining documents. 
## Vedi anche

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
