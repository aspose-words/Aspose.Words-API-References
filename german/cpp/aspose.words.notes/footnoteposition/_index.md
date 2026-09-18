---
title: "Aspose::Words::Notes::FootnotePosition enum"
linktitle: "FootnotePosition"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Notes::FootnotePosition enum. Definiert die Position der Fußnote in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.notes/footnoteposition/
---
## FootnotePosition enum


Definiert die Position der Fußnote.

```cpp
enum class FootnotePosition
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| BottomOfPage | 1 | Fußnoten werden am unteren Rand jeder Seite ausgegeben. |
| BeneathText | 2 | Fußnoten werden unter dem Text auf jeder Seite ausgegeben. |


## Beispiele



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

## Siehe auch

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
