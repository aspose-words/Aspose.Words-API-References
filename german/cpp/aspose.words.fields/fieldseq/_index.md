---
title: "Aspose::Words::Fields::FieldSeq Klasse"
linktitle: "FieldSeq"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldSeq Klasse. Implementiert das SEQ-Feld. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 91000
url: /de/cpp/aspose.words.fields/fieldseq/
---
## FieldSeq class


Implementiert das SEQ-Feld. Weitere Informationen finden Sie im [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) Dokumentationsartikel.

```cpp
class FieldSeq : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Liest oder legt einen Lesezeichennamen fest, der sich auf ein Element an anderer Stelle im Dokument bezieht und nicht auf die aktuelle Position. |
| [get_DisplayResult](../field/get_displayresult/)() | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [get_End](../field/get_end/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldEnd](../field/get_fieldend/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldStart](../field/get_fieldstart/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Format](../field/get_format/)() | Liefert ein [FieldFormat](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Feldes bietet. |
| [get_InsertNextNumber](./get_insertnextnumber/)() | Liest oder legt fest, ob die nächste Sequenznummer für das angegebene Element eingefügt werden soll. |
| [get_IsDirty](../field/get_isdirty/)() | Liefert oder setzt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [get_IsLocked](../field/get_islocked/)() | Liefert oder setzt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [get_LocaleId](../field/get_localeid/)() | Liefert oder setzt die LCID des Feldes. |
| [get_ResetHeadingLevel](./get_resetheadinglevel/)() | Liest oder legt eine ganze Zahl fest, die die Überschriftenebene angibt, auf die die Sequenznummer zurückgesetzt werden soll. Gibt -1 zurück, wenn die Zahl fehlt. |
| [get_ResetNumber](./get_resetnumber/)() | Liest oder legt eine ganze Zahl fest, auf die die Sequenznummer zurückgesetzt werden soll. Gibt -1 zurück, wenn die Zahl fehlt. |
| [get_Result](../field/get_result/)() | Liefert oder setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [get_Separator](../field/get_separator/)() | Liefert den Knoten, der das Feldtrennzeichen darstellt. Kann **null** sein. |
| [get_SequenceIdentifier](./get_sequenceidentifier/)() | Liest oder legt den Namen fest, der der Reihe von zu nummerierenden Elementen zugewiesen wird. |
| [get_Start](../field/get_start/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| virtual [get_Type](../field/get_type/)() const | Liefert den Microsoft‑Word-Feldtyp. |
| [GetFieldCode](../field/getfieldcode/)() | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Feldes das letzte Kind seines übergeordneten Knotens ist, gibt es den übergeordneten Absatz zurück. Wenn das Feld bereits entfernt wurde, gibt es **null** zurück. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldSeq::get_BookmarkName](./get_bookmarkname/). |
| [set_InsertNextNumber](./set_insertnextnumber/)(bool) | Setter für [Aspose::Words::Fields::FieldSeq::get_InsertNextNumber](./get_insertnextnumber/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter für [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ResetHeadingLevel](./set_resetheadinglevel/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldSeq::get_ResetHeadingLevel](./get_resetheadinglevel/). |
| [set_ResetNumber](./set_resetnumber/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldSeq::get_ResetNumber](./get_resetnumber/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter für [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceIdentifier](./set_sequenceidentifier/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier](./get_sequenceidentifier/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Führt das Entlinken des Feldes aus. |
| [Update](../field/update/)() | Führt das Aktualisieren des Feldes aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
| [Update](../field/update/)(bool) | Führt ein Feld-Update aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |

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


Zeigt das Erstellen von Nummerierungen mit SEQ‑Feldern.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// SEQ-Felder zeigen einen Zähler an, der bei jedem SEQ-Feld inkrementiert wird.
// Diese Felder führen zudem separate Zähler für jede eindeutig benannte Sequenz
// identifiziert durch die "SequenceIdentifier"-Eigenschaft des SEQ-Feldes.
// Fügen Sie ein SEQ‑Feld ein, das den aktuellen Zählwert von "MySequence" anzeigt,
// nachdem die Eigenschaft "ResetNumber" verwendet wurde, um sie auf 100 zu setzen.
builder->Write(u"#");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetNumber(u"100");
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\r 100", fieldSeq->GetFieldCode());
ASSERT_EQ(u"100", fieldSeq->get_Result());

// Zeigen Sie die nächste Nummer in dieser Sequenz mit einem weiteren SEQ‑Feld an.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->Update();

ASSERT_EQ(u"101", fieldSeq->get_Result());

// Fügen Sie eine Überschrift der Ebene 1 ein.
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"This level 1 heading will reset MySequence to 1");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));

// Fügen Sie ein weiteres SEQ‑Feld aus derselben Sequenz ein und konfigurieren Sie es so, dass die Zählung bei jeder Überschrift mit 1 zurückgesetzt wird.
builder->Write(u"\n#");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetHeadingLevel(u"1");
fieldSeq->Update();

// Die obige Überschrift ist eine Überschrift der Ebene 1, sodass die Zählung für diese Sequenz auf 1 zurückgesetzt wird.
ASSERT_EQ(u" SEQ  MySequence \\s 1", fieldSeq->GetFieldCode());
ASSERT_EQ(u"1", fieldSeq->get_Result());

// Gehen Sie zur nächsten Nummer dieser Sequenz.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_InsertNextNumber(true);
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\n", fieldSeq->GetFieldCode());
ASSERT_EQ(u"2", fieldSeq->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.ResetNumbering.docx");
```


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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
