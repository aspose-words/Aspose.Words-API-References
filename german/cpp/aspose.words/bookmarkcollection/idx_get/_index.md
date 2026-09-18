---
title: "Aspose::Words::BookmarkCollection::idx_get method"
linktitle: "idx_get"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BookmarkCollection::idx_get method. Gibt ein Lesezeichen nach Name in C++ zurück."
type: docs
weight: 6000
url: /de/cpp/aspose.words/bookmarkcollection/idx_get/
---
## BookmarkCollection::idx_get(const System::String\&) method


Gibt ein Lesezeichen anhand des Namens zurück.

```cpp
System::SharedPtr<Aspose::Words::Bookmark> Aspose::Words::BookmarkCollection::idx_get(const System::String &bookmarkName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkName | const System::String\& | Groß-/Kleinschreibungsunabhängiger Name des Lesezeichens. |
## Hinweise


Gibt **null** zurück, wenn das Lesezeichen mit dem angegebenen Namen nicht gefunden werden kann.

## Siehe auch

* Class [Bookmark](../../bookmark/)
* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## BookmarkCollection::idx_get(int32_t) method


Gibt ein Lesezeichen am angegebenen Index zurück.

```cpp
System::SharedPtr<Aspose::Words::Bookmark> Aspose::Words::BookmarkCollection::idx_get(int32_t index)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Ein Index in die Sammlung. |
## Hinweise


Der Index ist nullbasiert.

Negative Indizes sind erlaubt und bedeuten Zugriff vom Ende der Sammlung. Zum Beispiel bedeutet -1 das letzte Element, -2 das vorletzte und so weiter.

Wenn der Index größer als oder gleich der Anzahl der Elemente in der Liste ist, gibt dies eine Nullreferenz zurück.

Wenn der Index negativ ist und sein absoluter Wert größer ist als die Anzahl der Elemente in der Liste, gibt dies eine Nullreferenz zurück.

## Siehe auch

* Class [Bookmark](../../bookmark/)
* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
