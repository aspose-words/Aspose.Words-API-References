---
title: "Aspose::Words::Notes::FootnoteOptions::get_StartNumber Methode"
linktitle: "get_StartNumber"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Notes::FootnoteOptions::get_StartNumber Methode. Gibt die Startnummer oder das Zeichen für die erste automatisch nummerierte Fußnote in C++ an."
type: docs
weight: 6000
url: /de/cpp/aspose.words.notes/footnoteoptions/get_startnumber/
---
## FootnoteOptions::get_StartNumber method


Gibt die Startzahl oder das Startzeichen für die erste automatisch nummerierte Fußnote an.

```cpp
int32_t Aspose::Words::Notes::FootnoteOptions::get_StartNumber() override
```

## Hinweise


Diese Eigenschaft wirkt nur, wenn [RestartRule](../get_restartrule/) auf [Continuous](../../footnotenumberingrule/) gesetzt ist.

## Beispiele



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

* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
