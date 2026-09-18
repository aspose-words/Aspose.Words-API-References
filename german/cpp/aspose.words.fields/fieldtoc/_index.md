---
title: "Aspose::Words::Fields::FieldToc Klasse"
linktitle: "FieldToc"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldToc Klasse. Implementiert das TOC-Feld. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 105000
url: /de/cpp/aspose.words.fields/fieldtoc/
---
## FieldToc class


Implementiert das TOC-Feld. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldToc : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [FieldToc](./fieldtoc/)() |  |
| [get_BookmarkName](./get_bookmarkname/)() | Ermittelt den Namen des Lesezeichens, das den Teil des Dokuments markiert, der zum Erstellen der Tabelle verwendet wird. |
| [get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/)() | Liest oder setzt den Namen des Sequenzidentifikators, der beim Erstellen eines Abbildungsverzeichnisses verwendet wird, das die Beschriftungsbezeichnung und -nummer nicht enthält. |
| [get_CustomStyles](./get_customstyles/)() | Liest eine Liste von Formatvorlagen, die von den integrierten Überschriftenformatvorlagen abweichen und im Inhaltsverzeichnis aufgenommen werden sollen. |
| [get_DisplayResult](../field/get_displayresult/)() | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [get_End](../field/get_end/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_EntryIdentifier](./get_entryidentifier/)() | Liest eine Zeichenkette, die mit den Typbezeichnern der einzuschließenden TC-Felder übereinstimmen soll. |
| [get_EntryLevelRange](./get_entrylevelrange/)() | Liest einen Bereich von Ebenen der Inhaltsverzeichniseinträge, die aufgenommen werden sollen. |
| [get_EntrySeparator](./get_entryseparator/)() | Liest eine Zeichenfolge, die einen Eintrag und seine Seitenzahl trennt. |
| [get_FieldEnd](../field/get_fieldend/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldStart](../field/get_fieldstart/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Format](../field/get_format/)() | Liefert ein [FieldFormat](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Feldes bietet. |
| [get_HeadingLevelRange](./get_headinglevelrange/)() | Liest einen Bereich von Überschriftenebenen, die aufgenommen werden sollen. |
| [get_HideInWebLayout](./get_hideinweblayout/)() | Liest, ob Tabulator-Führungszeichen und Seitenzahlen in der Weblayout-Ansicht ausgeblendet werden sollen. |
| [get_InsertHyperlinks](./get_inserthyperlinks/)() | Liest, ob die Einträge des Inhaltsverzeichnisses als Hyperlinks dargestellt werden sollen. |
| [get_IsDirty](../field/get_isdirty/)() | Liefert oder setzt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [get_IsLocked](../field/get_islocked/)() | Liefert oder setzt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [get_LocaleId](../field/get_localeid/)() | Liefert oder setzt die LCID des Feldes. |
| [get_PageNumberOmittingLevelRange](./get_pagenumberomittinglevelrange/)() | Liest einen Bereich von Ebenen der Inhaltsverzeichniseinträge, aus denen Seitenzahlen weggelassen werden sollen. |
| [get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/)() | Liest oder setzt den Bezeichner einer Sequenz, für die dem Seitenzahlen-Eintrag ein Präfix hinzugefügt werden soll. |
| [get_PreserveLineBreaks](./get_preservelinebreaks/)() | Liest, ob Zeilenumbruchzeichen innerhalb von Tabelleneinträgen erhalten bleiben sollen. |
| [get_PreserveTabs](./get_preservetabs/)() | Liest, ob Tabulator-Einträge innerhalb von Tabelleneinträgen erhalten bleiben sollen. |
| [get_Result](../field/get_result/)() | Liefert oder setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [get_Separator](../field/get_separator/)() | Liefert den Knoten, der das Feldtrennzeichen darstellt. Kann **null** sein. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Liest oder setzt die Zeichenfolge, die verwendet wird, um Sequenznummern und Seitenzahlen zu trennen. |
| [get_Start](../field/get_start/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_TableOfFiguresLabel](./get_tableoffigureslabel/)() | Liest oder setzt den Namen des Sequenzidentifikators, der beim Erstellen eines Abbildungsverzeichnisses verwendet wird. |
| virtual [get_Type](../field/get_type/)() const | Liefert den Microsoft‑Word-Feldtyp. |
| [get_UseParagraphOutlineLevel](./get_useparagraphoutlinelevel/)() | Ermittelt, ob die angewandte Absatz-Gliederungsebene verwendet wird. |
| [GetFieldCode](../field/getfieldcode/)() | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Feldes das letzte Kind seines übergeordneten Knotens ist, gibt es den übergeordneten Absatz zurück. Wenn das Feld bereits entfernt wurde, gibt es **null** zurück. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Setzt den Namen des Lesezeichens, das den Teil des Dokuments markiert, der zum Erstellen der Tabelle verwendet wird. |
| [set_CaptionlessTableOfFiguresLabel](./set_captionlesstableoffigureslabel/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/). |
| [set_CustomStyles](./set_customstyles/)(const System::String\&) | Legt eine Liste von Formatvorlagen fest, die von den integrierten Überschriftsformatvorlagen abweichen und im Inhaltsverzeichnis enthalten sein sollen. |
| [set_EntryIdentifier](./set_entryidentifier/)(const System::String\&) | Legt eine Zeichenkette fest, die mit den Typkennungen der einzuschließenden TC-Felder übereinstimmen soll. |
| [set_EntryLevelRange](./set_entrylevelrange/)(const System::String\&) | Legt einen Bereich von Ebenen der Inhaltsverzeichniseinträge fest, die eingeschlossen werden sollen. |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | Legt eine Zeichenfolge fest, die einen Eintrag und seine Seitenzahl trennt. |
| [set_HeadingLevelRange](./set_headinglevelrange/)(const System::String\&) | Legt einen Bereich von Überschriftsstufen fest, die eingeschlossen werden sollen. |
| [set_HideInWebLayout](./set_hideinweblayout/)(bool) | Legt fest, ob Tabulator-Führungszeichen und Seitenzahlen in der Weblayout-Ansicht ausgeblendet werden. |
| [set_InsertHyperlinks](./set_inserthyperlinks/)(bool) | Legt fest, ob die Einträge des Inhaltsverzeichnisses Hyperlinks werden. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter für [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberOmittingLevelRange](./set_pagenumberomittinglevelrange/)(const System::String\&) | Legt einen Bereich von Ebenen der Inhaltsverzeichniseinträge fest, für die Seitenzahlen weggelassen werden. |
| [set_PrefixedSequenceIdentifier](./set_prefixedsequenceidentifier/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldToc::get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/). |
| [set_PreserveLineBreaks](./set_preservelinebreaks/)(bool) | Legt fest, ob Zeilenumbruchzeichen innerhalb von Tabelleneinträgen erhalten bleiben. |
| [set_PreserveTabs](./set_preservetabs/)(bool) | Legt fest, ob Tabulator-Einträge innerhalb von Tabelleneinträgen erhalten bleiben. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter für [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldToc::get_SequenceSeparator](./get_sequenceseparator/). |
| [set_TableOfFiguresLabel](./set_tableoffigureslabel/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldToc::get_TableOfFiguresLabel](./get_tableoffigureslabel/). |
| [set_UseParagraphOutlineLevel](./set_useparagraphoutlinelevel/)(bool) | Legt fest, ob die angewandte Absatz-Gliederungsebene verwendet wird. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Führt das Entlinken des Feldes aus. |
| [Update](../field/update/)() | Führt das Aktualisieren des Feldes aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
| [Update](../field/update/)(bool) | Führt ein Feld-Update aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
| [UpdatePageNumbers](./updatepagenumbers/)() | Aktualisiert die Seitenzahlen für die Elemente in diesem Inhaltsverzeichnis. |

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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
