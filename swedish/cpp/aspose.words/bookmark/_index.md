---
title: "Aspose::Words::Bookmark-klass"
linktitle: "Bokmärke"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Bookmark-klass. Representerar ett enskilt bokmärke. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/bookmark/
---
## Bookmark class


Representerar ett enskilt bokmärke. För att lära dig mer, besök artikeln [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/) documentation article.

```cpp
class Bookmark : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_BookmarkEnd](./get_bookmarkend/)() | Hämtar noden som representerar slutet på bokmärket. |
| [get_BookmarkStart](./get_bookmarkstart/)() const | Hämtar noden som representerar början på bokmärket. |
| [get_FirstColumn](./get_firstcolumn/)() | Hämtar det nollbaserade indexet för den första kolumnen i tabellkolumnintervallet som är associerat med bokmärket. |
| [get_IsColumn](./get_iscolumn/)() | Returnerar **true** om detta bokmärke är ett tabellkolumnbokmärke. |
| [get_LastColumn](./get_lastcolumn/)() | Hämtar det nollbaserade indexet för den sista kolumnen i tabellkolumnintervallet som är associerat med bokmärket. |
| [get_Name](./get_name/)() | Hämtar eller anger namnet på bokmärket. |
| [get_Text](./get_text/)() | Hämtar texten som är omsluten av bokmärket. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Tar bort bokmärket från dokumentet. Tar inte bort texten inuti bokmärket. |
| [set_Name](./set_name/)(const System::String\&) | Sättare för [Aspose::Words::Bookmark::get_Name](./get_name/). |
| [set_Text](./set_text/)(const System::String\&) | Anger texten som är omsluten av bokmärket. |
| static [Type](./type/)() |  |
## Anmärkningar


[Bookmark](./) is a "facade" object that encapsulates two nodes [BookmarkStart](./get_bookmarkstart/) and [BookmarkEnd](./get_bookmarkend/) in a document tree and allows to work with a bookmark as a single object. 
## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
