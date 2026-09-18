---
title: "Aspose::Words::Comment::get_Id method"
linktitle: "get_Id"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Comment::get_Id method. Gibt die Kommentar-ID zurück oder setzt sie in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words/comment/get_id/
---
## Comment::get_Id method


Liest oder setzt die Kommentar-ID.

```cpp
int32_t Aspose::Words::Comment::get_Id() const
```

## Hinweise


Die Kommentar-ID ermöglicht es, einen Kommentar an einem Textbereich im Dokument zu verankern. Der Bereich muss mit dem [CommentRangeStart](../../commentrangestart/)- und dem [CommentRangeEnd](../../commentrangeend/)-Objekt markiert werden, die denselben Identifikatorwert wie das [Comment](../)-Objekt teilen.

Sie würden diesen Wert verwenden, wenn Sie nach den [CommentRangeStart](../../commentrangestart/)- und [CommentRangeEnd](../../commentrangeend/)-Knoten suchen, die mit diesem Kommentar verknüpft sind.

[Comment](../) identifiers are supposed to be unique across a document and Aspose.Words automatically maintains comment identifiers when loading, saving and combining documents. 
## Siehe auch

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
