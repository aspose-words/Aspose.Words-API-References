---
title: "Aspose::Words::Fields::FieldXE::get_IsBold Methode"
linktitle: "get_IsBold"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldXE::get_IsBold Methode. Ermittelt oder legt fest, ob die fette Formatierung auf die Seitenzahl des Eintrags in C++ angewendet wird."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fields/fieldxe/get_isbold/
---
## FieldXE::get_IsBold method


Liest oder setzt, ob die Seitenzahl des Eintrags fett formatiert werden soll.

```cpp
bool Aspose::Words::Fields::FieldXE::get_IsBold()
```


## Beispiele



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

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
