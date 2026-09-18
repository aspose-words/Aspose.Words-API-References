---
title: "Aspose::Words::Notes::EndnoteOptions::get_NumberStyle Methode"
linktitle: "get_NumberStyle"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Notes::EndnoteOptions::get_NumberStyle Methode. Gibt das Zahlenformat für automatisch nummerierte Endnoten in C++ an."
type: docs
weight: 2000
url: /de/cpp/aspose.words.notes/endnoteoptions/get_numberstyle/
---
## EndnoteOptions::get_NumberStyle method


Gibt das Zahlenformat für automatisch nummerierte Endnoten an.

```cpp
Aspose::Words::NumberStyle Aspose::Words::Notes::EndnoteOptions::get_NumberStyle() override
```

## Hinweise


Nicht alle Zahlenformate sind für diese Eigenschaft anwendbar. Für die Liste der anwendbaren Zahlenformate siehe das Einfügen‑Dialogfeld für [Footnote](../../footnote/) oder Endnote in Microsoft Word. Wenn Sie ein Zahlenformat auswählen, das nicht anwendbar ist, stellt Microsoft Word auf einen Standardwert zurück.

## Beispiele



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

## Siehe auch

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
