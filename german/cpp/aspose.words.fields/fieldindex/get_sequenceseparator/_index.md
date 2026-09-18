---
title: "Aspose::Words::Fields::FieldIndex::get_SequenceSeparator Methode"
linktitle: "get_SequenceSeparator"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldIndex::get_SequenceSeparator Methode. Gibt die Zeichenfolge zurück oder legt sie fest, die verwendet wird, um Sequenznummern und Seitenzahlen in C++ zu trennen."
type: docs
weight: 16000
url: /de/cpp/aspose.words.fields/fieldindex/get_sequenceseparator/
---
## FieldIndex::get_SequenceSeparator method


Liest oder setzt die Zeichenfolge, die verwendet wird, um Sequenznummern und Seitenzahlen zu trennen.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_SequenceSeparator()
```


## Beispiele



Zeigt, wie man ein Dokument in Abschnitte aufteilt, indem man INDEX- und SEQ-Felder kombiniert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstelle ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt den Text‑Eigenschaftswert des XE-Feldes auf der linken Seite an,
// und die Seitenzahl, die das XE-Feld enthält, auf der rechten Seite.
// Wenn die XE-Felder denselben Wert in ihrer "Text"‑Eigenschaft haben,
// wird das INDEX-Feld sie zu einem Eintrag zusammenfassen.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// In der SequenceName-Eigenschaft geben Sie eine SEQ-Feldsequenz an. Jeder Eintrag dieses INDEX-Feldes wird nun auch anzeigen
// die Nummer, bei der der Sequenzzähler am XE-Feldstandort steht, der diesen Eintrag erstellt hat.
index->set_SequenceName(u"MySequence");

// Legen Sie Text fest, der um die Sequenz- und Seitenzahlen herum angezeigt wird, um deren Bedeutung dem Benutzer zu erklären.
// Ein mit dieser Konfiguration erstellter Eintrag zeigt etwa "MySequence at 1 on page 1" bei seiner Seitenzahl an.
// PageNumberSeparator und SequenceSeparator dürfen nicht länger als 15 Zeichen sein.
index->set_PageNumberSeparator(u"\tMySequence at ");
index->set_SequenceSeparator(u" on page ");
ASSERT_TRUE(index->get_HasSequenceName());

ASSERT_EQ(u" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index->GetFieldCode());

// SEQ-Felder zeigen einen Zähler an, der bei jedem SEQ-Feld inkrementiert wird.
// Diese Felder führen zudem separate Zähler für jede eindeutig benannte Sequenz
// identifiziert durch die "SequenceIdentifier"-Eigenschaft des SEQ-Feldes.
// Fügen Sie ein SEQ-Feld ein, das die "MySequence"-Sequenz auf 1 verschiebt.
// Dieses Feld unterscheidet sich nicht von normalem Dokumenttext. Es wird nicht im Inhaltsverzeichnis eines INDEX-Feldes erscheinen.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", sequenceField->GetFieldCode());

// Fügen Sie ein XE-Feld ein, das einen Eintrag im INDEX-Feld erstellt.
// Da "MySequence" bei 1 steht und dieses XE-Feld auf Seite 2 ist, zusammen mit den oben definierten benutzerdefinierten Trennzeichen,
// wird der INDEX-Eintrag dieses Feldes "Cat" auf der linken Seite und "MySequence at 1 on page 2" auf der rechten Seite anzeigen.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

ASSERT_EQ(u" XE  Cat", indexEntry->GetFieldCode());

// Fügen Sie einen Seitenumbruch ein und verwenden Sie SEQ-Felder, um "MySequence" auf 3 zu erhöhen.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

// Fügen Sie ein XE-Feld mit derselben Text-Eigenschaft wie das obige ein.
// Der INDEX-Eintrag gruppiert XE-Felder mit übereinstimmenden Werten in der "Text"-Eigenschaft.
// zu einem Eintrag, anstatt für jedes XE-Feld einen eigenen Eintrag zu erstellen.
// Da wir auf Seite 2 sind und "MySequence" bei 3 steht, wird ", 3 on page 3" an denselben INDEX-Eintrag wie oben angehängt.
// Der Seitenzahl-Teil dieses INDEX-Eintrags wird nun "MySequence at 1 on page 2, 3 on page 3" anzeigen.
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

// Fügen Sie ein XE-Feld mit einem neuen und eindeutigen Text-Eigenschaftswert ein.
// Dies fügt einen neuen Eintrag hinzu, mit MySequence bei 3 auf Seite 4.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Dog");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Sequence.docx");
```

## Siehe auch

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
