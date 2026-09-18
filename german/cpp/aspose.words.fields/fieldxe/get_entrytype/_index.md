---
title: "Aspose::Words::Fields::FieldXE::get_EntryType Methode"
linktitle: "get_EntryType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldXE::get_EntryType Methode. Liest oder legt einen Indexeintragstyp fest in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldxe/get_entrytype/
---
## FieldXE::get_EntryType method


Liest oder setzt einen Indexeintragstyp.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_EntryType()
```


## Beispiele



Zeigt, wie man ein INDEX-Feld erstellt und anschließend XE-Felder verwendet, um es mit Einträgen zu füllen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstelle ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt den Wert der Text‑Eigenschaft des XE-Feldes auf der linken Seite
// und die Seite, die das XE-Feld enthält, auf der rechten Seite.
// Wenn die XE-Felder denselben Wert in ihrer "Text"‑Eigenschaft haben,
// wird das INDEX-Feld sie zu einem Eintrag zusammenfassen.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Konfiguriere das INDEX-Feld so, dass es nur XE-Felder anzeigt, die innerhalb der Grenzen
// eines Lesezeichens namens "MainBookmark" liegen und deren "EntryType"‑Eigenschaften den Wert "A" haben.
// Für sowohl INDEX- als auch XE-Felder verwendet die "EntryType"‑Eigenschaft nur das erste Zeichen ihres Zeichenkettenwerts.
index->set_BookmarkName(u"MainBookmark");
index->set_EntryType(u"A");

ASSERT_EQ(u" INDEX  \\b MainBookmark \\f A", index->GetFieldCode());

// Auf einer neuen Seite starte das Lesezeichen mit einem Namen, der dem Wert entspricht
// der "BookmarkName"‑Eigenschaft des INDEX-Feldes.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MainBookmark");

// Das INDEX-Feld wird diesen Eintrag erfassen, weil er sich innerhalb des Lesezeichens befindet,
// und sein Eintragstyp stimmt ebenfalls mit dem Eintragstyp des INDEX-Feldes überein.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 1");
indexEntry->set_EntryType(u"A");

ASSERT_EQ(u" XE  \"Index entry 1\" \\f A", indexEntry->GetFieldCode());

// Fügen Sie ein XE-Feld ein, das nicht im INDEX erscheint, weil die Eintragstypen nicht übereinstimmen.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 2");
indexEntry->set_EntryType(u"B");

// Beenden Sie das Lesezeichen und fügen Sie anschließend ein XE-Feld ein.
// Es ist vom selben Typ wie das INDEX-Feld, wird aber nicht angezeigt
// da es sich außerhalb der Grenzen des Lesezeichens befindet.
builder->EndBookmark(u"MainBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 3");
indexEntry->set_EntryType(u"A");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Filtering.docx");
```

## Siehe auch

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
