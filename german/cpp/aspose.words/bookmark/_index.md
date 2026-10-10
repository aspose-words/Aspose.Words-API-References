---
title: "Aspose::Words::Bookmark Klasse"
linktitle: "Lesezeichen"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Bookmark Klasse. Stellt ein einzelnes Lesezeichen dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words/bookmark/
---
## Bookmark class


Stellt ein einzelnes Lesezeichen dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class Bookmark : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_BookmarkEnd](./get_bookmarkend/)() | Gibt den Knoten zurück, der das Ende des Lesezeichens darstellt. |
| [get_BookmarkStart](./get_bookmarkstart/)() const | Gibt den Knoten zurück, der den Anfang des Lesezeichens darstellt. |
| [get_FirstColumn](./get_firstcolumn/)() | Gibt den nullbasierten Index der ersten Spalte des Tabellen‑Spaltenbereichs zurück, der dem Lesezeichen zugeordnet ist. |
| [get_IsColumn](./get_iscolumn/)() | Gibt **true** zurück, wenn dieses Lesezeichen ein Tabellen‑Spalten‑Lesezeichen ist. |
| [get_LastColumn](./get_lastcolumn/)() | Gibt den nullbasierten Index der letzten Spalte des Tabellen‑Spaltenbereichs zurück, der dem Lesezeichen zugeordnet ist. |
| [get_Name](./get_name/)() | Liest oder setzt den Namen des Lesezeichens. |
| [get_Text](./get_text/)() | Liest den im Lesezeichen eingeschlossenen Text. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Entfernt das Lesezeichen aus dem Dokument. Entfernt nicht den Text innerhalb des Lesezeichens. |
| [set_Name](./set_name/)(const System::String\&) | Setter für [Aspose::Words::Bookmark::get_Name](./get_name/). |
| [set_Text](./set_text/)(const System::String\&) | Setzt den im Lesezeichen eingeschlossenen Text. |
| static [Type](./type/)() |  |
## Hinweise


[Bookmark](./) is a "facade" object that encapsulates two nodes [BookmarkStart](./get_bookmarkstart/) and [BookmarkEnd](./get_bookmarkend/) in a document tree and allows to work with a bookmark as a single object. 
## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
