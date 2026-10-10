---
title: "Aspose::Words::Notes::EndnotePosition‑Enum"
linktitle: "EndnotePosition"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Notes::EndnotePosition‑Enum. Definiert die Endnotenposition in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.notes/endnoteposition/
---
## EndnotePosition enum


Definiert die Position der Endnote.

```cpp
enum class EndnotePosition
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| EndOfSection | 0 | Endnoten werden am Ende des Abschnitts ausgegeben. |
| EndOfDocument | 3 | Endnoten werden am Ende des Dokuments ausgegeben. |


## Beispiele



Zeigt, wie ein anderer Ort ausgewählt wird, an dem das Dokument seine Endnoten sammelt und anzeigt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Eine Endnote ist eine Möglichkeit, einen Verweis oder einen Randkommentar an Text anzuhängen
// die den Fluss des Haupttextes nicht stört.
// Das Einfügen einer Endnote fügt ein kleines hochgestelltes Referenzsymbol hinzu
// im Haupttext dort, wo wir die Endnote einfügen.
// Jede Endnote erstellt ebenfalls einen Eintrag am Ende des Dokuments, bestehend aus einem Symbol
// der dem Referenzsymbol im Haupttext entspricht.
// Der Referenztext, den wir an die "InsertEndnote"-Methode des Dokumenten‑Builders übergeben.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote contents.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"This is the second section.");

// Wir können die Eigenschaft "Position" verwenden, um zu bestimmen, wo das Dokument alle seine Endnoten platziert.
// Wenn wir den Wert der Eigenschaft "Position" auf "EndnotePosition.EndOfDocument" setzen,
// wird jede Fußnote in einer Sammlung am Ende des Dokuments angezeigt. Dies ist der Standardwert.
// Wenn wir den Wert der Eigenschaft "Position" auf "EndnotePosition.EndOfSection" setzen,
// wird jede Fußnote in einer Sammlung am Ende des Abschnitts angezeigt, dessen Text die Referenzmarke der Endnote enthält.
doc->get_EndnoteOptions()->set_Position(endnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionEndnote.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
