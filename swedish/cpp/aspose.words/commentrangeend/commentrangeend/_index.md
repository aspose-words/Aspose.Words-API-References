---
title: "Aspose::Words::CommentRangeEnd::CommentRangeEnd konstruktor"
linktitle: "CommentRangeEnd"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::CommentRangeEnd::CommentRangeEnd konstruktor. Initierar en ny instans av denna klass i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/commentrangeend/commentrangeend/
---
## CommentRangeEnd::CommentRangeEnd constructor


Initierar en ny instans av den här klassen.

```cpp
Aspose::Words::CommentRangeEnd::CommentRangeEnd(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, int32_t id)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Ägandokumentet. |
| id | int32_t | Kommentaridentifieraren som detta objekt är länkat till. |
## Anmärkningar


När [CommentRangeEnd](../) skapas tillhör den det angivna dokumentet, men är ännu inte en del av dokumentet och [ParentNode](../../node/get_parentnode/) är **null**.

För att lägga till ett [CommentRangeEnd](../) i dokumentet, använd InsertAfter eller InsertBefore på det stycke där du vill att kommentaren ska infogas.

## Se även

* Class [DocumentBase](../../documentbase/)
* Class [CommentRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
