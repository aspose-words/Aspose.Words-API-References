---
title: "Aspose::Words::BookmarkCollection Klasse"
linktitle: "BookmarkCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BookmarkCollection Klasse. Eine Sammlung von Bookmark-Objekten, die die Lesezeichen im angegebenen Bereich darstellen. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words/bookmarkcollection/
---
## BookmarkCollection class


Eine Sammlung von [Bookmark](../bookmark/) Objekten, die die Lesezeichen im angegebenen Bereich darstellen. Weitere Informationen finden Sie im [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/) Dokumentationsartikel.

```cpp
class BookmarkCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bookmark>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Clear](./clear/)() | Entfernt alle Lesezeichen aus dieser Sammlung und aus dem Dokument. |
| [get_Count](./get_count/)() | Gibt die Anzahl der Lesezeichen in der Sammlung zurück. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator-Objekt zurück. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gibt ein Lesezeichen am angegebenen Index zurück. |
| [idx_get](./idx_get/)(const System::String\&) | Gibt ein Lesezeichen anhand des Namens zurück. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Bookmark\>\&) | Entfernt das angegebene Lesezeichen aus dem Dokument. |
| [Remove](./remove/)(const System::String\&) | Entfernt ein Lesezeichen mit dem angegebenen Namen. |
| [RemoveAt](./removeat/)(int32_t) | Entfernt ein Lesezeichen am angegebenen Index. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
