---
title: "Aspose::Words::Fields::FieldIndex Klasse"
linktitle: "FieldIndex"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldIndex Klasse. Implementiert das INDEX-Feld. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 59000
url: /de/cpp/aspose.words.fields/fieldindex/
---
## FieldIndex class


Implementiert das INDEX-Feld. Weitere Informationen finden Sie im [Arbeiten mit Feldern](https://docs.aspose.com/words/cpp/working-with-fields/) Dokumentationsartikel.

```cpp
class FieldIndex : public Aspose::Words::Fields::Field,
                   public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Liest oder setzt den Namen des Lesezeichens, das den Teil des Dokuments markiert, der zum Erstellen des Index verwendet wird. |
| [get_CrossReferenceSeparator](./get_crossreferenceseparator/)() | Liest oder setzt die Zeichenfolge, die verwendet wird, um Querverweise und andere Einträge zu trennen. |
| [get_DisplayResult](../field/get_displayresult/)() | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [get_End](../field/get_end/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_EntryType](./get_entrytype/)() | Liest oder setzt einen Indexeintragstyp, der zum Erstellen des Index verwendet wird. |
| [get_FieldEnd](../field/get_fieldend/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldStart](../field/get_fieldstart/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Format](../field/get_format/)() | Liefert ein [FieldFormat](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Feldes bietet. |
| [get_HasPageNumberSeparator](./get_haspagenumberseparator/)() | Liest einen Wert, der angibt, ob ein Seitenzahltrennzeichen durch den Feldcode überschrieben wird. |
| [get_HasSequenceName](./get_hassequencename/)() | Liest einen Wert, der angibt, ob eine Sequenz beim Erstellen des Feldergebnisses verwendet werden soll. |
| [get_Heading](./get_heading/)() | Liest oder setzt eine Überschrift, die am Anfang jeder Gruppe von Einträgen für einen bestimmten Buchstaben erscheint. |
| [get_IsDirty](../field/get_isdirty/)() | Liefert oder setzt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [get_IsLocked](../field/get_islocked/)() | Liefert oder setzt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [get_LanguageId](./get_languageid/)() | Liest oder setzt die Sprach-ID, die zum Erzeugen des Index verwendet wird. |
| [get_LetterRange](./get_letterrange/)() | Liest oder setzt einen Buchstabenbereich, auf den der Index beschränkt wird. |
| [get_LocaleId](../field/get_localeid/)() | Liefert oder setzt die LCID des Feldes. |
| [get_NumberOfColumns](./get_numberofcolumns/)() | Liest oder setzt die Anzahl der Spalten pro Seite, die beim Erstellen des Index verwendet werden. |
| [get_PageNumberListSeparator](./get_pagenumberlistseparator/)() | Liest oder setzt die Zeichenfolge, die verwendet wird, um zwei Seitenzahlen in einer Seitenzahlenliste zu trennen. |
| [get_PageNumberSeparator](./get_pagenumberseparator/)() | Liest oder setzt die Zeichenfolge, die verwendet wird, um einen Indexeintrag und seine Seitenzahl zu trennen. |
| [get_PageRangeSeparator](./get_pagerangeseparator/)() | Liest oder setzt die Zeichenfolge, die verwendet wird, um den Anfang und das Ende eines Seitenbereichs zu trennen. |
| [get_Result](../field/get_result/)() | Liefert oder setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [get_RunSubentriesOnSameLine](./get_runsubentriesonsameline/)() | Liest oder setzt, ob Untereinträge in derselben Zeile wie der Haupteintrag angezeigt werden. |
| [get_Separator](../field/get_separator/)() | Liefert den Knoten, der das Feldtrennzeichen darstellt. Kann **null** sein. |
| [get_SequenceName](./get_sequencename/)() | Liest oder setzt den Namen einer Sequenz, deren Nummer mit der Seitenzahl angegeben wird. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Liest oder setzt die Zeichenfolge, die verwendet wird, um Sequenznummern und Seitenzahlen zu trennen. |
| [get_Start](../field/get_start/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| virtual [get_Type](../field/get_type/)() const | Liefert den Microsoft‑Word-Feldtyp. |
| [get_UseYomi](./get_useyomi/)() | Liest oder setzt, ob die Verwendung von Yomi-Text für Indexeinträge aktiviert werden soll. |
| [GetFieldCode](../field/getfieldcode/)() | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Feldes das letzte Kind seines übergeordneten Knotens ist, gibt es den übergeordneten Absatz zurück. Wenn das Feld bereits entfernt wurde, gibt es **null** zurück. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldIndex::get_BookmarkName](./get_bookmarkname/). |
| [set_CrossReferenceSeparator](./set_crossreferenceseparator/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator](./get_crossreferenceseparator/). |
| [set_EntryType](./set_entrytype/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldIndex::get_EntryType](./get_entrytype/). |
| [set_Heading](./set_heading/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldIndex::get_Heading](./get_heading/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LanguageId](./set_languageid/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldIndex::get_LanguageId](./get_languageid/). |
| [set_LetterRange](./set_letterrange/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldIndex::get_LetterRange](./get_letterrange/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter für [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_NumberOfColumns](./set_numberofcolumns/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldIndex::get_NumberOfColumns](./get_numberofcolumns/). |
| [set_PageNumberListSeparator](./set_pagenumberlistseparator/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldIndex::get_PageNumberListSeparator](./get_pagenumberlistseparator/). |
| [set_PageNumberSeparator](./set_pagenumberseparator/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldIndex::get_PageNumberSeparator](./get_pagenumberseparator/). |
| [set_PageRangeSeparator](./set_pagerangeseparator/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator](./get_pagerangeseparator/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter für [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_RunSubentriesOnSameLine](./set_runsubentriesonsameline/)(bool) | Setter für [Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine](./get_runsubentriesonsameline/). |
| [set_SequenceName](./set_sequencename/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldIndex::get_SequenceName](./get_sequencename/). |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldIndex::get_SequenceSeparator](./get_sequenceseparator/). |
| [set_UseYomi](./set_useyomi/)(bool) | Setter für [Aspose::Words::Fields::FieldIndex::get_UseYomi](./get_useyomi/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Führt das Entlinken des Feldes aus. |
| [Update](../field/update/)() | Führt das Aktualisieren des Feldes aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
| [Update](../field/update/)(bool) | Führt ein Feld-Update aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |

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


Zeigt, wie man ein INDEX-Feld mit Einträgen über XE-Felder füllt und zudem sein Aussehen anpasst.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstelle ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt den Text‑Eigenschaftswert des XE-Feldes auf der linken Seite an,
// und die Seitenzahl, die das XE-Feld enthält, auf der rechten Seite.
// Wenn die XE-Felder denselben Wert in ihrer "Text"‑Eigenschaft haben,
// wird das INDEX-Feld sie zu einem Eintrag zusammenfassen.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_LanguageId(u"1033");

// Wenn dieser Eigenschaftswert auf "A" gesetzt wird, werden alle Einträge nach ihrem ersten Buchstaben gruppiert,
// und dieser Buchstabe wird in Großbuchstaben über jeder Gruppe platziert.
index->set_Heading(u"A");

// Legen Sie fest, dass die vom INDEX-Feld erstellte Tabelle über 2 Spalten hinweg reicht.
index->set_NumberOfColumns(u"2");

// Lassen Sie Einträge mit Anfangsbuchstaben außerhalb des Zeichenbereichs "a-c" aus.
index->set_LetterRange(u"a-c");

ASSERT_EQ(u" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index->GetFieldCode());

// Die nächsten beiden XE-Felder werden unter der Überschrift "A" angezeigt,
// wobei ihre jeweiligen Textformatierungen ebenfalls auf die Seitenzahlen angewendet werden.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");
indexEntry->set_IsItalic(true);

ASSERT_EQ(u" XE  Apple \\i", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apricot");
indexEntry->set_IsBold(true);

ASSERT_EQ(u" XE  Apricot \\b", indexEntry->GetFieldCode());

// Die beiden nächsten XE-Felder stehen unter den Überschriften "B" bzw. "C" im Inhaltsverzeichnis der INDEX-Felder.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cherry");

// INDEX-Felder sortieren alle Einträge alphabetisch, sodass dieser Eintrag zusammen mit den anderen beiden unter "A" angezeigt wird.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Avocado");

// Dieser Eintrag wird nicht angezeigt, weil er mit dem Buchstaben "D" beginnt,
// was außerhalb des Zeichenbereichs "a-c" liegt, den die LetterRange‑Eigenschaft des INDEX-Feldes definiert.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Durian");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Formatting.docx");
```

## Siehe auch

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
