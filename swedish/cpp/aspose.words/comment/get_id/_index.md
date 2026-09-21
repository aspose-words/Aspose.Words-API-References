---
title: "Aspose::Words::Comment::get_Id metod"
linktitle: "get_Id"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Comment::get_Id metod. Hämtar eller anger kommentaridentifieraren i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words/comment/get_id/
---
## Comment::get_Id method


Hämtar eller anger kommentarsidentifieraren.

```cpp
int32_t Aspose::Words::Comment::get_Id() const
```

## Anmärkningar


Kommentaridentifieraren möjliggör att ankra en kommentar till ett textområde i dokumentet. Området måste avgränsas med hjälp av objektet [CommentRangeStart](../../commentrangestart/) och [CommentRangeEnd](../../commentrangeend/) som delar samma identifieringsvärde som objektet [Comment](../).

Du skulle använda detta värde när du letar efter noderna [CommentRangeStart](../../commentrangestart/) och [CommentRangeEnd](../../commentrangeend/) som är länkade till denna kommentar.

[Comment](../) identifiers are supposed to be unique across a document and Aspose.Words automatically maintains comment identifiers when loading, saving and combining documents. 
## Se även

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
