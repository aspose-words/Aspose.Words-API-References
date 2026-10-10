---
title: "Aspose::Words::Notes::FootnoteNumberingRule enum"
linktitle: "FootnoteNumberingRule"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Notes::FootnoteNumberingRule enum. Bestimmt, wann die automatische Fußnoten‑ oder Endnoten‑Nummerierung in C++ neu startet."
type: docs
weight: 5000
url: /de/cpp/aspose.words.notes/footnotenumberingrule/
---
## FootnoteNumberingRule enum


Bestimmt, wann die automatische Nummerierung von Fußnoten oder Endnoten neu startet.

```cpp
enum class FootnoteNumberingRule
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Continuous | 0 | Durchgängige Nummerierung im gesamten Dokument. |
| RestartSection | 1 | Nummerierung startet in jedem Abschnitt neu. |
| RestartPage | 2 | Nummerierung startet auf jeder Seite neu. Gilt nur für Fußnoten. |
| Default | n/a | Gleich [Continuous](./). |


## Beispiele



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

## Siehe auch

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
