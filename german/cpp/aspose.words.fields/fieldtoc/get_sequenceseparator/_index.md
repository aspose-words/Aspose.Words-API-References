---
title: "Aspose::Words::Fields::FieldToc::get_SequenceSeparator Methode"
linktitle: "get_SequenceSeparator"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldToc::get_SequenceSeparator Methode. Gibt die Zeichenfolge zurück oder legt sie fest, die verwendet wird, um Sequenznummern und Seitenzahlen in C++ zu trennen."
type: docs
weight: 17000
url: /de/cpp/aspose.words.fields/fieldtoc/get_sequenceseparator/
---
## FieldToc::get_SequenceSeparator method


Liest oder setzt die Zeichenfolge, die verwendet wird, um Sequenznummern und Seitenzahlen zu trennen.

```cpp
System::String Aspose::Words::Fields::FieldToc::get_SequenceSeparator()
```


## Beispiele



Zeigt, wie man ein TOC-Feld mit Einträgen unter Verwendung von SEQ-Feldern füllt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ein TOC-Feld kann für jedes im Dokument gefundene SEQ-Feld einen Eintrag im Inhaltsverzeichnis erzeugen.
// Jeder Eintrag enthält den Absatz, der das SEQ-Feld enthält, und die Seitenzahl, auf der das Feld erscheint.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// SEQ-Felder zeigen einen Zähler an, der bei jedem SEQ-Feld inkrementiert wird.
// Diese Felder führen zudem separate Zähler für jede eindeutig benannte Sequenz
// identifiziert durch die "SequenceIdentifier"-Eigenschaft des SEQ-Feldes.
// Verwenden Sie die "TableOfFiguresLabel"-Eigenschaft, um eine Hauptsequenz für das TOC zu benennen.
// Jetzt wird dieses TOC nur Einträge aus SEQ-Feldern erstellen, deren "SequenceIdentifier" auf "MySequence" gesetzt ist.
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Wir können eine weitere SEQ-Feldsequenz in der "PrefixedSequenceIdentifier"-Eigenschaft benennen.
// SEQ-Felder aus dieser Präfixsequenz werden keine TOC-Einträge erzeugen.
// Jeder aus einem SEQ-Feld der Hauptsequenz erstellte TOC-Eintrag wird jetzt auch die Anzahl anzeigen, die
// die Präfixsequenz aktuell hat, beim primären Sequenz-SEQ-Feld, das den Eintrag erzeugt hat.
fieldToc->set_PrefixedSequenceIdentifier(u"PrefixSequence");

// Jeder TOC-Eintrag wird die Präfixsequenzanzahl sofort links von
// der Seitenzahl anzeigen, auf der das SEQ-Feld der Hauptsequenz erscheint.
// Wir können einen benutzerdefinierten Trenner festlegen, der zwischen diesen beiden Zahlen erscheint.
fieldToc->set_SequenceSeparator(u">");

ASSERT_EQ(u" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Es gibt zwei Möglichkeiten, SEQ-Felder zu verwenden, um dieses TOC zu füllen.
// 1 -  Einfügen eines SEQ-Feldes, das zur Präfixsequenz des TOC gehört:
// Dieses Feld wird den SEQ-Sequenzzähler für die "PrefixSequence" um 1 erhöhen.
// Da dieses Feld nicht zur identifizierten Hauptsequenz gehört
// durch die "TableOfFiguresLabel"-Eigenschaft des TOC, wird es nicht als Eintrag erscheinen.
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();

ASSERT_EQ(u" SEQ  PrefixSequence", fieldSeq->GetFieldCode());

// 2 -  Einfügen eines SEQ-Feldes, das zur Hauptsequenz des TOC gehört:
// Dieses SEQ-Feld wird einen Eintrag im TOC erzeugen.
// Der TOC-Eintrag wird den Absatz enthalten, in dem das SEQ-Feld steht, sowie die Seitenzahl, auf der es erscheint.
// Dieser Eintrag wird auch die aktuelle Zählung der Präfixsequenz anzeigen,
// getrennt von der Seitenzahl durch den Wert in der Eigenschaft SeqenceSeparator des TOC.
// Die "PrefixSequence"-Zählung ist bei 1, dieses Hauptsequenz SEQ Feld ist auf Seite 2,
// und das Trennzeichen ist ">", also wird der Eintrag "1>2" anzeigen.
builder->Write(u"First TOC entry, MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", fieldSeq->GetFieldCode());

// Fügen Sie eine Seite ein, erhöhen Sie die Präfixsequenz um 2 und fügen Sie anschließend ein SEQ‑Feld ein, um einen TOC‑Eintrag zu erstellen.
// Die Präfixsequenz ist jetzt bei 2, und das Hauptsequenz‑SEQ‑Feld befindet sich auf Seite 3,
// so wird der TOC‑Eintrag "2>3" bei seiner Seitenzahl anzeigen.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
builder->Write(u"Second TOC entry, MySequence #");
fieldSeq->set_SequenceIdentifier(u"MySequence");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TOC.SEQ.docx");
```

## Siehe auch

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
