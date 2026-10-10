---
title: "Aspose::Words::Layout::LayoutEntityType‑enum"
linktitle: "LayoutEntityType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::LayoutEntityType‑enum. Typer av layout‑entiteter i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enum


Typer av layout‑entiteter.

```cpp
enum class LayoutEntityType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | n/a | Standardvärde. |
| Page | n/a | Representerar en sida i ett dokument. En sida kan ha [Column](./), [HeaderFooter](./) och [Comment](./) underordnade entiteter. |
| Column | n/a | Representerar en kolumn med text på en sida. Kolumnen kan ha samma underordnade enheter som [Cell](./), samt [Footnote](./), [Endnote](./) och [NoteSeparator](./) enheter. |
| Row | n/a | Representerar en tabellrad. Raden kan ha [Cell](./) som underordnade enheter. |
| Cell | n/a | Representerar en tabellcell. Cellen kan ha [Line](./) och [Row](./) underordnade enheter. |
| Line | n/a | Representerar en rad med tecken av text och inbäddade objekt. Raden kan ha [Span](./) underordnade enheter. |
| Span | n/a | Representerar en eller flera tecken i en rad. Detta inkluderar specialtecken som fältstart-/slutmärken, bokmärken och kommentarer. Span får inte ha underordnade enheter. |
| Footnote | n/a | Representerar en platshållare för fotnotens innehåll. Fotnoten kan ha [Note](./) underordnade enheter. |
| Endnote | n/a | Representerar en platshållare för slutnotens innehåll. Slutnoten kan ha [Note](./) underordnade enheter. |
| Note | n/a | Representerar en platshållare för notens innehåll. Noten kan ha [Line](./) och [Row](./) underordnade enheter. |
| HeaderFooter | n/a | Representerar en platshållare för sidhuvud-/sidfotens innehåll på en sida. [HeaderFooter](../../aspose.words/headerfooter/) kan ha [Line](./) och [Row](./) underordnade enheter. |
| TextBox | n/a | Representerar ett textområde inuti en form. Textbox kan ha [Line](./) och [Row](./) underordnade enheter. |
| Comment | n/a | Representerar en platshållare för kommentarinnehåll. [Comment](../../aspose.words/comment/) kan ha [Line](./) och [Row](./) underordnade enheter. |
| NoteSeparator | n/a | Representerar fotnot-/slutnotseparator. NoteSeparator kan ha [Line](./) och [Row](./) underordnade enheter. |

## Se även

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
