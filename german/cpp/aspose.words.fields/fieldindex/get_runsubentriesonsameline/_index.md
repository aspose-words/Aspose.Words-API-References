---
title: "Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine Methode"
linktitle: "get_RunSubentriesOnSameLine"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine Methode. Liest oder setzt, ob Untereinträge in dieselbe Zeile wie der Haupteintrag in C++ geschrieben werden."
type: docs
weight: 14000
url: /de/cpp/aspose.words.fields/fieldindex/get_runsubentriesonsameline/
---
## FieldIndex::get_RunSubentriesOnSameLine method


Liest oder setzt, ob Untereinträge in derselben Zeile wie der Haupteintrag angezeigt werden.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine()
```


## Beispiele



Zeigt, wie man mit Untereinträgen in einem INDEX-Feld arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstelle ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt den Text‑Eigenschaftswert des XE-Feldes auf der linken Seite an,
// und die Seitenzahl, die das XE-Feld enthält, auf der rechten Seite.
// Der INDEX-Eintrag sammelt alle XE-Felder mit übereinstimmenden Werten in der \"Text\"-Eigenschaft.
// zu einem Eintrag, anstatt für jedes XE-Feld einen eigenen Eintrag zu erstellen.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_PageNumberSeparator(u", see page ");
index->set_Heading(u"A");

// XE-Felder, die eine Text-Eigenschaft besitzen, deren Wert zur Überschrift des INDEX-Eintrags wird.
// Wenn dieser Wert zwei Zeichenketten‑Segmente enthält, die durch einen Doppelpunkt getrennt sind (der INDEX‑Eintrag behandelt :) als Trennzeichen,
// ist das erste Segment die Überschrift und das zweite Segment wird zur Unterüberschrift.
// Das INDEX‑Feld gruppiert Einträge zuerst alphabetisch und dann, wenn es mehrere XE‑Felder mit derselben
// Überschrift gibt, wird das INDEX‑Feld sie weiter nach den Werten dieser Überschriften unterteilen.
// Es kann mehrere Untergruppierungsebenen geben, abhängig davon, wie oft
// die Text‑Eigenschaften von XE‑Feldern auf diese Weise segmentiert werden.
// Standardmäßig erstellt eine INDEX‑Feldeintragsgruppe für jede Unterüberschrift innerhalb dieser Gruppe eine neue Zeile.
// Wir können das Flag RunSubentriesOnSameLine auf true setzen, um die Überschrift beizubehalten,
// und jede Unterüberschrift der Gruppe stattdessen in einer Zeile zu halten, wodurch das INDEX‑Feld kompakter wird.
index->set_RunSubentriesOnSameLine(runSubentriesOnTheSameLine);

if (runSubentriesOnTheSameLine)
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A \\r", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A", index->GetFieldCode());
}

// Fügen Sie zwei XE‑Felder ein, jedes auf einer neuen Seite, und mit derselben Überschrift namens "Heading 1",
// die das INDEX‑Feld zur Gruppierung verwendet.
// Wenn RunSubentriesOnSameLine false ist, erstellt die INDEX‑Tabelle drei Zeilen:
// eine Zeile für die Gruppierungsüberschrift "Heading 1" und jeweils eine weitere Zeile für jede Unterüberschrift.
// Wenn RunSubentriesOnSameLine true ist, erstellt die INDEX‑Tabelle eine einzeilige
// Eintrag, der die Überschrift und alle Unterüberschriften umfasst.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Heading 1:Subheading 1");

ASSERT_EQ(u" XE  \"Heading 1:Subheading 1\"", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Heading 1:Subheading 2");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + System::String::Format(u"Field.INDEX.XE.Subheading.docx"));
```

## Siehe auch

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
