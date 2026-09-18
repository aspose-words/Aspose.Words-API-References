---
title: "Aspose::Words::Bookmark::get_Name Methode"
linktitle: "get_Name"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Bookmark::get_Name Methode. Gibt den Namen des Lesezeichens zurück oder setzt ihn in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words/bookmark/get_name/
---
## Bookmark::get_Name method


Liest oder setzt den Namen des Lesezeichens.

```cpp
System::String Aspose::Words::Bookmark::get_Name()
```


## Beispiele



Zeigt, wie man ein Lesezeichen einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ein gültiges Lesezeichen hat einen Namen, einen BookmarkStart- und einen BookmarkEnd-Knoten.
// Alle Leerzeichen in den Namen von Lesezeichen werden in Unterstriche umgewandelt, wenn wir das gespeicherte Dokument mit Microsoft Word öffnen.
// Wenn wir den Namen des Lesezeichens in Microsoft Word über Einfügen -> Links -> Lesezeichen markieren und "Gehe zu",
// Der Cursor springt zum Text, der zwischen den BookmarkStart- und BookmarkEnd-Knoten eingeschlossen ist.
builder->StartBookmark(u"My Bookmark");
builder->Write(u"Contents of MyBookmark.");
builder->EndBookmark(u"My Bookmark");

// Lesezeichen werden in dieser Sammlung gespeichert.
ASSERT_EQ(u"My Bookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());

doc->Save(get_ArtifactsDir() + u"Bookmarks.Insert.docx");
```

## Siehe auch

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
