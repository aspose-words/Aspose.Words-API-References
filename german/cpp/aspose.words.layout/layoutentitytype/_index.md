---
title: "Aspose::Words::Layout::LayoutEntityType Enum"
linktitle: "LayoutEntityType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::LayoutEntityType Enum. Typen der Layout-Entitäten in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enum


Typen der Layout-Entitäten.

```cpp
enum class LayoutEntityType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | n/a | Standardwert. |
| Page | n/a | Stellt eine Seite eines Dokuments dar. Eine Seite kann die Kind-Entitäten [Column](./), [HeaderFooter](./) und [Comment](./) besitzen. |
| Column | n/a | Stellt eine Textspalte auf einer Seite dar. Eine Spalte kann die gleichen Kind-Entitäten wie [Cell](./) haben, zusätzlich die Entitäten [Footnote](./), [Endnote](./) und [NoteSeparator](./). |
| Row | n/a | Stellt eine Tabellenzeile dar. Eine Zeile kann [Cell](./) als Kind-Entität haben. |
| Cell | n/a | Stellt eine Tabellenzelle dar. Eine Zelle kann die Kind-Entitäten [Line](./) und [Row](./) haben. |
| Line | n/a | Stellt eine Zeile von Zeichen des Textes und Inline-Objekten dar. Eine Zeile kann die Kind-Entität [Span](./) haben. |
| Span | n/a | Stellt ein oder mehrere Zeichen in einer Zeile dar. Dies schließt Sonderzeichen wie Feld‑Start/End‑Markierungen, Lesezeichen und Kommentare ein. Span darf keine Kind-Entitäten haben. |
| Footnote | n/a | Stellt einen Platzhalter für Fußnoteninhalte dar. Fußnote kann die Kind-Entität [Note](./) haben. |
| Endnote | n/a | Stellt einen Platzhalter für Endnoteninhalte dar. Endnote kann die Kind-Entität [Note](./) haben. |
| Note | n/a | Stellt einen Platzhalter für Notizinhalte dar. Note kann die Kind-Entitäten [Line](./) und [Row](./) haben. |
| HeaderFooter | n/a | Stellt einen Platzhalter für Kopf‑/Fußzeilen‑Inhalte auf einer Seite dar. [HeaderFooter](../../aspose.words/headerfooter/) kann die Kind-Entitäten [Line](./) und [Row](./) haben. |
| TextBox | n/a | Stellt einen Textbereich innerhalb einer Form dar. Textbox kann die Kind-Entitäten [Line](./) und [Row](./) haben. |
| Comment | n/a | Stellt einen Platzhalter für Kommentar‑Inhalte dar. [Comment](../../aspose.words/comment/) kann die Kind-Entitäten [Line](./) und [Row](./) haben. |
| NoteSeparator | n/a | Stellt einen Fußnoten/Endnoten‑Trenner dar. NoteSeparator kann die Kind-Entitäten [Line](./) und [Row](./) haben. |

## Siehe auch

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
