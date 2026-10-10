---
title: "Aspose::Words::BookmarkEnd::Accept‑metod"
linktitle: "Accept"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BookmarkEnd::Accept‑metod. Accepterar en besökare i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/bookmarkend/accept/
---
## BookmarkEnd::Accept method


Accepterar en besökare.

```cpp
bool Aspose::Words::BookmarkEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| besökare | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Besökaren som kommer att besöka noden. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Anmärkningar


Anropar [VisitBookmarkEnd()](../../documentvisitor/visitbookmarkend/).

För mer information, se Visitor-designmönstret.

## Se även

* Class [DocumentVisitor](../../documentvisitor/)
* Class [BookmarkEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
