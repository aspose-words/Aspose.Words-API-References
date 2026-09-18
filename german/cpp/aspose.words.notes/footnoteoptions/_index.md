---
title: "Aspose::Words::Notes::FootnoteOptions Klasse"
linktitle: "FootnoteOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Notes::FootnoteOptions Klasse. Stellt die Optionen für die Fußnotennummerierung für ein Dokument oder einen Abschnitt dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.notes/footnoteoptions/
---
## FootnoteOptions class


Stellt die Nummerierungsoptionen für Fußnoten in einem Dokument oder Abschnitt dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Footnote and Endnote](https://docs.aspose.com/words/cpp/working-with-footnote-and-endnote/).

```cpp
class FootnoteOptions : public Aspose::Words::Notes::IFootnoteOptions
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Columns](./get_columns/)() | Gibt die Anzahl der Spalten an, mit denen der Fußnotenbereich formatiert wird. |
| [get_NumberStyle](./get_numberstyle/)() override | Gibt das Zahlenformat für automatisch nummerierte Fußnoten an. |
| [get_Position](./get_position/)() | Gibt die Position der Fußnoten an. |
| [get_RestartRule](./get_restartrule/)() override | Bestimmt, wann die automatische Nummerierung neu startet. |
| [get_StartNumber](./get_startnumber/)() override | Gibt die Startzahl oder das Startzeichen für die erste automatisch nummerierte Fußnote an. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Columns](./set_columns/)(int32_t) | Setter für [Aspose::Words::Notes::FootnoteOptions::get_Columns](./get_columns/). |
| [set_NumberStyle](./set_numberstyle/)(Aspose::Words::NumberStyle) override | Setter für [Aspose::Words::Notes::FootnoteOptions::get_NumberStyle](./get_numberstyle/). |
| [set_Position](./set_position/)(Aspose::Words::Notes::FootnotePosition) | Setter für [Aspose::Words::Notes::FootnoteOptions::get_Position](./get_position/). |
| [set_RestartRule](./set_restartrule/)(Aspose::Words::Notes::FootnoteNumberingRule) override | Setter für [Aspose::Words::Notes::FootnoteOptions::get_RestartRule](./get_restartrule/). |
| [set_StartNumber](./set_startnumber/)(int32_t) override | Setter für [Aspose::Words::Notes::FootnoteOptions::get_StartNumber](./get_startnumber/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man den Fußnotenabschnitt in eine gegebene Anzahl von Spalten aufteilt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

doc->get_FootnoteOptions()->set_Columns(2);
doc->Save(get_ArtifactsDir() + u"Document.FootnoteColumns.docx");
```


Zeigt, wie man einen anderen Ort auswählt, an dem das Dokument seine Fußnoten sammelt und anzeigt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Eine Fußnote ist eine Möglichkeit, einen Verweis oder einen Randkommentar an Text anzuhängen
// die den Fluss des Haupttextes nicht stört.
// Das Einfügen einer Fußnote fügt ein kleines hochgestelltes Referenzsymbol hinzu
// im Haupttext, wo wir die Fußnote einfügen.
// Jede Fußnote erstellt außerdem einen Eintrag am unteren Rand der Seite, bestehend aus einem Symbol
// der dem Referenzsymbol im Haupttext entspricht.
// Der Referenztext, den wir an die \"InsertFootnote\"‑Methode des Dokumenten‑Builders übergeben.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote contents.");

// Wir können die Eigenschaft \"Position\" verwenden, um zu bestimmen, wo das Dokument alle seine Fußnoten platziert.
// Wenn wir den Wert der Eigenschaft \"Position\" auf \"FootnotePosition.BottomOfPage\" setzen,
// wird jede Fußnote am unteren Rand der Seite angezeigt, die ihr Referenzzeichen enthält. Dies ist der Standardwert.
// Wenn wir den Wert der Eigenschaft \"Position\" auf \"FootnotePosition.BeneathText\" setzen,
// wird jede Fußnote am Ende des Textes der Seite angezeigt, die ihr Referenzzeichen enthält.
doc->get_FootnoteOptions()->set_Position(footnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionFootnote.docx");
```


Zeigt, wie man den Zahlenstil von Fußnoten‑/Endnoten‑Referenzzeichen ändert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fußnoten und Endnoten sind eine Möglichkeit, einen Verweis oder einen Randkommentar an Text anzuhängen
// die den Fluss des Haupttextes nicht stört.
// Das Einfügen einer Fußnote/eines Endnotiz fügt ein kleines hochgestelltes Referenzsymbol hinzu
// im Haupttext, wo wir die Fußnote/Endnote einfügen.
// Jede Fußnote/Endnote erstellt außerdem einen Eintrag, der aus einem Symbol besteht, das dem Referenzzeichen entspricht
// Symbol im Haupttext. Der Referenztext, den wir an die \"InsertEndnote\"‑Methode des Dokumenten‑Builders übergeben.
// Fußnoteneinträge werden standardmäßig am unteren Rand jeder Seite angezeigt, die
// ihre Referenzsymbole enthält, und Endnoten werden am Ende des Dokuments angezeigt.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.", u"Custom footnote reference mark");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.", u"Custom endnote reference mark");

// Standardmäßig ist das Referenzsymbol für jede Fußnote und Endnote ihr Index
// unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument führt separate Zähler
// für Fußnoten und für Endnoten. Standardmäßig zeigen Fußnoten ihre Nummern mit arabischen Ziffern an,
// und Endnoten zeigen ihre Nummern in kleinen römischen Ziffern an.
ASSERT_EQ(Aspose::Words::NumberStyle::Arabic, doc->get_FootnoteOptions()->get_NumberStyle());
ASSERT_EQ(Aspose::Words::NumberStyle::LowercaseRoman, doc->get_EndnoteOptions()->get_NumberStyle());

// Wir können die Eigenschaft \"NumberStyle\" verwenden, um benutzerdefinierte Nummerierungsstile auf Fußnoten und Endnoten anzuwenden.
// Dies wirkt sich nicht auf Fußnoten/Endnoten mit benutzerdefinierten Referenzzeichen aus.
doc->get_FootnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);

doc->Save(get_ArtifactsDir() + u"InlineStory.RefMarkNumberStyle.docx");
```


Zeigt, wie man die Nummerierung von Fußnoten/Endnoten an bestimmten Stellen im Dokument neu startet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fußnoten und Endnoten sind eine Möglichkeit, einen Verweis oder einen Randkommentar an Text anzuhängen
// die den Fluss des Haupttextes nicht stört.
// Das Einfügen einer Fußnote/eines Endnotiz fügt ein kleines hochgestelltes Referenzsymbol hinzu
// im Haupttext, wo wir die Fußnote/Endnote einfügen.
// Jede Fußnote/Endnote erstellt außerdem einen Eintrag, der aus einem Symbol besteht, das dem Referenzzeichen entspricht
// Symbol im Haupttext. Der Referenztext, den wir an die \"InsertEndnote\"‑Methode des Dokumenten‑Builders übergeben.
// Fußnoteneinträge werden standardmäßig am unteren Rand jeder Seite angezeigt, die
// ihre Referenzsymbole enthält, und Endnoten werden am Ende des Dokuments angezeigt.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 4.");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 4.");

// Standardmäßig ist das Referenzsymbol für jede Fußnote und Endnote ihr Index
// unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument führt separate Zähler
// für Fußnoten und Endnoten und setzt diese Zähler zu keinem Zeitpunkt zurück.
ASSERT_EQ(doc->get_FootnoteOptions()->get_RestartRule(), Aspose::Words::Notes::FootnoteNumberingRule::Default);
ASSERT_EQ(Aspose::Words::Notes::FootnoteNumberingRule::Default, Aspose::Words::Notes::FootnoteNumberingRule::Continuous);

// Wir können die Eigenschaft \"RestartRule\" verwenden, um das Dokument zum Neustart zu veranlassen
// die Fußnoten-/Endnoten‑Zählungen beginnen auf einer neuen Seite oder in einem Abschnitt.
doc->get_FootnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
doc->get_EndnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartSection);

doc->Save(get_ArtifactsDir() + u"InlineStory.NumberingRule.docx");
```


Zeigt, wie man eine Zahl festlegt, bei der das Dokument die Fußnoten-/Endnoten‑Zählung beginnt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fußnoten und Endnoten sind eine Möglichkeit, einen Verweis oder einen Randkommentar an Text anzuhängen
// die den Fluss des Haupttextes nicht stört.
// Das Einfügen einer Fußnote/eines Endnotiz fügt ein kleines hochgestelltes Referenzsymbol hinzu
// im Haupttext, wo wir die Fußnote/Endnote einfügen.
// Jede Fußnote/Endnote erstellt außerdem einen Eintrag, der aus einem Symbol besteht
// der dem Referenzsymbol im Haupttext entspricht.
// Der Referenztext, den wir an die "InsertEndnote"-Methode des Dokumenten‑Builders übergeben.
// Fußnoteneinträge werden standardmäßig am unteren Rand jeder Seite angezeigt, die
// ihre Referenzsymbole enthält, und Endnoten werden am Ende des Dokuments angezeigt.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");

// Standardmäßig ist das Referenzsymbol für jede Fußnote und Endnote ihr Index
// unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument führt separate Zähler
// für Fußnoten und Endnoten, die beide bei 1 beginnen.
ASSERT_EQ(1, doc->get_FootnoteOptions()->get_StartNumber());
ASSERT_EQ(1, doc->get_EndnoteOptions()->get_StartNumber());

// Wir können die Eigenschaft "StartNumber" verwenden, um das Dokument dazu zu bringen
// eine Fußnoten‑ oder Endnoten‑Zählung mit einer anderen Zahl zu beginnen.
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::Arabic);
doc->get_EndnoteOptions()->set_StartNumber(50);

doc->Save(get_ArtifactsDir() + u"InlineStory.StartNumber.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
