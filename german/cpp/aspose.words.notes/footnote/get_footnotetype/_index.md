---
title: "Aspose::Words::Notes::Footnote::get_FootnoteType Methode"
linktitle: "get_FootnoteType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Notes::Footnote::get_FootnoteType Methode. Gibt einen Wert zurück, der angibt, ob es sich um eine Fußnote oder Endnote handelt, in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.notes/footnote/get_footnotetype/
---
## Footnote::get_FootnoteType method


Gibt einen Wert zurück, der angibt, ob es sich um eine Fußnote oder Endnote handelt.

```cpp
Aspose::Words::Notes::FootnoteType Aspose::Words::Notes::Footnote::get_FootnoteType() const
```


## Beispiele



Zeigt den Unterschied zwischen Fußnoten und Endnoten.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Im Folgenden werden zwei Methoden zum Anfügen nummerierter Verweise zum Text gezeigt. Beide Verweise fügen ein
// kleines hochgestelltes Verweiszeichen an der Stelle, an der wir sie einfügen.
// Das Verweiszeichen ist standardmäßig die Indexnummer des Verweises unter allen Verweisen im Dokument.
// Jeder Verweis erstellt außerdem einen Eintrag, der dasselbe Verweiszeichen wie im Fließtext hat.
// und Referenztext, den wir an die Methode "InsertFootnote" des Dokumenten‑Builders übergeben.
// 1 -  Eine Fußnote, deren Eintrag auf derselben Seite wie der referenzierte Text erscheint:
builder->Write(u"Footnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 -  Eine Endnote, deren Eintrag am Ende des Dokuments erscheint:
builder->Write(u"Endnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> endnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote text, will appear at the very end of the document.");

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Footnote, footnote->get_FootnoteType());
ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Endnote, endnote->get_FootnoteType());

doc->Save(get_ArtifactsDir() + u"InlineStory.FootnoteEndnote.docx");
```

## Siehe auch

* Enum [FootnoteType](../../footnotetype/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
