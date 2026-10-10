---
title: "Aspose::Words::Fields::FieldXE::get_PageRangeBookmarkName Methode"
linktitle: "get_PageRangeBookmarkName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldXE::get_PageRangeBookmarkName Methode. Gibt den Namen des Lesezeichens zurück oder legt ihn fest, das einen Seitenbereich markiert, der als Seitenzahl des Eintrags in C++ eingefügt wird."
type: docs
weight: 6000
url: /de/cpp/aspose.words.fields/fieldxe/get_pagerangebookmarkname/
---
## FieldXE::get_PageRangeBookmarkName method


Liest oder setzt den Namen des Lesezeichens, das einen Seitenbereich markiert, der als Seitenzahl des Eintrags eingefügt wird.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_PageRangeBookmarkName()
```


## Beispiele



Zeigt, wie man die von einem Lesezeichen umfassten Seiten als Seitenbereich für einen INDEX-Feldeintrag festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstelle ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt den Text‑Eigenschaftswert des XE-Feldes auf der linken Seite an,
// und die Seitenzahl, die das XE-Feld enthält, auf der rechten Seite.
// Der INDEX-Eintrag sammelt alle XE-Felder mit übereinstimmenden Werten in der \"Text\"-Eigenschaft.
// zu einem Eintrag, anstatt für jedes XE-Feld einen eigenen Eintrag zu erstellen.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Für INDEX-Einträge, die Seitenbereiche anzeigen, können wir einen Trenner‑String angeben
// der zwischen der Nummer der ersten Seite und der Nummer der letzten Seite erscheint.
index->set_PageNumberSeparator(u", on page(s) ");
index->set_PageRangeSeparator(u" to ");

ASSERT_EQ(u" INDEX  \\e \", on page(s) \" \\g \" to \"", index->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"My entry");

// Wenn ein XE-Feld ein Lesezeichen mit der PageRangeBookmarkName‑Eigenschaft benennt,
// sein INDEX-Eintrag zeigt den Seitenbereich, den das Lesezeichen umfasst
// statt der Seitenzahl der Seite, die das XE-Feld enthält.
indexEntry->set_PageRangeBookmarkName(u"MyBookmark");

ASSERT_EQ(u" XE  \"My entry\" \\r MyBookmark", indexEntry->GetFieldCode());
ASSERT_EQ(u"MyBookmark", indexEntry->get_PageRangeBookmarkName());

// Fügen Sie ein Lesezeichen ein, das auf Seite 3 beginnt und auf Seite 5 endet.
// Der INDEX-Eintrag für das XE-Feld, das auf dieses Lesezeichen verweist, zeigt diesen Seitenbereich an.
// In unserer Tabelle wird der INDEX-Eintrag "My entry, on page(s) 3 to 5" anzeigen.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Start of MyBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"End of MyBookmark");
builder->EndBookmark(u"MyBookmark");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.PageRangeBookmark.docx");
```

## Siehe auch

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
