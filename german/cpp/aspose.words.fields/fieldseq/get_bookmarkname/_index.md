---
title: "Aspose::Words::Fields::FieldSeq::get_BookmarkName Methode"
linktitle: "get_BookmarkName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldSeq::get_BookmarkName Methode. Liest oder setzt einen Lesezeichen‑Namen, der sich auf ein Element an anderer Stelle im Dokument bezieht, nicht auf die aktuelle Position in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldseq/get_bookmarkname/
---
## FieldSeq::get_BookmarkName method


Liest oder legt einen Lesezeichennamen fest, der sich auf ein Element an anderer Stelle im Dokument bezieht und nicht auf die aktuelle Position.

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_BookmarkName()
```


## Beispiele



Zeigt, wie man Inhaltsverzeichnis‑ und Sequenzfelder kombiniert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ein TOC-Feld kann für jedes im Dokument gefundene SEQ-Feld einen Eintrag im Inhaltsverzeichnis erzeugen.
// Jeder Eintrag enthält den Absatz, der das SEQ‑Feld enthält,
// und die Seitenzahl, auf der das Feld erscheint.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// Konfigurieren Sie dieses TOC‑Feld so, dass es eine SequenceIdentifier‑Eigenschaft mit dem Wert "MySequence" hat.
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Konfigurieren Sie dieses TOC‑Feld so, dass es nur SEQ‑Felder übernimmt, die innerhalb der Grenzen eines Lesezeichens liegen
// mit dem Namen "TOCBookmark".
fieldToc->set_BookmarkName(u"TOCBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

ASSERT_EQ(u" TOC  \\c MySequence \\b TOCBookmark", fieldToc->GetFieldCode());

// SEQ-Felder zeigen einen Zähler an, der bei jedem SEQ-Feld inkrementiert wird.
// Diese Felder führen zudem separate Zähler für jede eindeutig benannte Sequenz
// identifiziert durch die "SequenceIdentifier"-Eigenschaft des SEQ-Feldes.
// Fügen Sie ein SEQ‑Feld ein, das einen Sequenz‑Identifier hat, der dem des TOC entspricht
// TableOfFiguresLabel‑Eigenschaft. Dieses Feld wird keinen Eintrag im TOC erzeugen, da es außerhalb
// der durch "BookmarkName" festgelegten Lesezeichen‑Grenzen liegt.
builder->Write(u"MySequence #");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will not show up in the TOC because it is outside of the bookmark.");

builder->StartBookmark(u"TOCBookmark");

// Die Sequenz dieses SEQ‑Feldes stimmt mit der "TableOfFiguresLabel"‑Eigenschaft des TOC überein und liegt innerhalb der Lesezeichen‑Grenzen.
// Der Absatz, der dieses Feld enthält, wird im Inhaltsverzeichnis als Eintrag angezeigt.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will show up in the TOC next to the entry for the above caption.");

// Die Sequenz dieses SEQ-Feldes stimmt nicht mit der "TableOfFiguresLabel"-Eigenschaft des Inhaltsverzeichnisses überein,
// und liegt innerhalb der Grenzen des Lesezeichens. Sein Absatz wird im Inhaltsverzeichnis nicht als Eintrag angezeigt.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"OtherSequence");
builder->Writeln(u", will not show up in the TOC because it's from a different sequence identifier.");

// Die Sequenz dieses SEQ-Feldes stimmt mit der "TableOfFiguresLabel"-Eigenschaft des Inhaltsverzeichnisses überein und liegt innerhalb der Grenzen des Lesezeichens.
// Dieses Feld verweist außerdem auf ein anderes Lesezeichen. Der Inhalt dieses Lesezeichens wird im Inhaltsverzeichnis-Eintrag für dieses SEQ-Feld erscheinen.
// Das SEQ-Feld selbst wird den Inhalt dieses Lesezeichens nicht anzeigen.
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_BookmarkName(u"SEQBookmark");
ASSERT_EQ(u" SEQ  MySequence SEQBookmark", fieldSeq->GetFieldCode());

// Erstellen Sie ein Lesezeichen mit Inhalten, die aufgrund des oben genannten SEQ-Feldes, das darauf verweist, im Inhaltsverzeichnis-Eintrag angezeigt werden.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"SEQBookmark");
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", text from inside SEQBookmark.");
builder->EndBookmark(u"SEQBookmark");

builder->EndBookmark(u"TOCBookmark");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.Bookmark.docx");
```

## Siehe auch

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
