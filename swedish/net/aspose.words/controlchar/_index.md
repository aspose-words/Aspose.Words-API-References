---
title: ControlChar
second_title: Aspose.Words för .NET API Referens
description: Kontrolltecken som ofta påträffas i dokument.
type: docs
weight: 340
url: /sv/net/aspose.words/controlchar/
---
## ControlChar class

Kontrolltecken som ofta påträffas i dokument.

```csharp
public static class ControlChar
```

## Fält

| namn | Beskrivning |
| --- | --- |
| static readonly [Cell](../../aspose.words/controlchar/cell) | Slutet på en tabellcell eller slutet av en tabellrads tecken: "\x0007" eller "\a". |
| const [CellChar](../../aspose.words/controlchar/cellchar) | Slutet på en tabellcell eller slutet av en tabellrads tecken: (char)7 eller "\a". |
| static readonly [ColumnBreak](../../aspose.words/controlchar/columnbreak) | Slut på kolumntecken: "\x000e". |
| const [ColumnBreakChar](../../aspose.words/controlchar/columnbreakchar) | Slut på kolumn tecken: (char)14. |
| static readonly [Cr](../../aspose.words/controlchar/cr) | Vagnreturtecken: "\x000d" eller "\r". Samma som[`ParagraphBreak`](./paragraphbreak) . |
| static readonly [CrLf](../../aspose.words/controlchar/crlf) | Carriage return följt av radmatningstecken: "\x000d\x000a" eller "\r\n". Används inte som sådan i Microsoft Word-dokument, men används vanligtvis i textfiler för styckebrytningar. |
| const [DefaultTextInputChar](../../aspose.words/controlchar/defaulttextinputchar) | Detta är tecknet "o" som används som standardvärde i formulärfält för textinmatning. |
| const [FieldEndChar](../../aspose.words/controlchar/fieldendchar) | Slutet av MS Word-fälttecken: (char)21. |
| const [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar) | Fältseparatortecken separerar fältkoden från fältvärdet. Valfritt i vissa fält. Värde: (char)20. |
| const [FieldStartChar](../../aspose.words/controlchar/fieldstartchar) | Start av MS Word-fälttecken: (char)19. |
| static readonly [Lf](../../aspose.words/controlchar/lf) | Radmatningstecken: "\x000a" eller "\n". Samma som[`LineFeed`](./linefeed) . |
| static readonly [LineBreak](../../aspose.words/controlchar/linebreak) | Radbrytningstecken: "\x000b" eller "\v". |
| const [LineBreakChar](../../aspose.words/controlchar/linebreakchar) | Radbrytningstecken: (char)11 eller "\v". |
| static readonly [LineFeed](../../aspose.words/controlchar/linefeed) | Radmatningstecken: "\x000a" eller "\n". Samma som[`Lf`](./lf) . |
| const [LineFeedChar](../../aspose.words/controlchar/linefeedchar) | Radmatningstecken: (char)10 eller "\n". |
| const [NonBreakingHyphenChar](../../aspose.words/controlchar/nonbreakinghyphenchar) | Nonbreaking bindestreck i Microsoft Word är (char)30. |
| static readonly [NonBreakingSpace](../../aspose.words/controlchar/nonbreakingspace) | Ej avbrytande blanksteg: "\x00a0". |
| const [NonBreakingSpaceChar](../../aspose.words/controlchar/nonbreakingspacechar) | Non-breaking space character: (char)160. |
| const [OptionalHyphenChar](../../aspose.words/controlchar/optionalhyphenchar) | Valfritt bindestreck i Microsoft Word är (char)31. |
| static readonly [PageBreak](../../aspose.words/controlchar/pagebreak) | Sidbrytningstecken: "\x000c" eller "\f". Observera att den har samma värde som[`SectionBreak`](./sectionbreak) . |
| const [PageBreakChar](../../aspose.words/controlchar/pagebreakchar) | Sidbrytningstecken: (char)12 eller "\f". |
| static readonly [ParagraphBreak](../../aspose.words/controlchar/paragraphbreak) | Slut på stycketecknet: "\x000d" eller "\r". Samma som[`Cr`](./cr) |
| const [ParagraphBreakChar](../../aspose.words/controlchar/paragraphbreakchar) | Slut på stycket tecken: (char)13 eller "\r". |
| static readonly [SectionBreak](../../aspose.words/controlchar/sectionbreak) | Avsnittets sluttecken: "\x000c" eller "\f". Observera att den har samma värde som[`PageBreak`](./pagebreak) . |
| const [SectionBreakChar](../../aspose.words/controlchar/sectionbreakchar) | Avsnittets sluttecken: (char)12 eller "\f". |
| const [SpaceChar](../../aspose.words/controlchar/spacechar) | Mellanslagstecken: (char)32. |
| static readonly [Tab](../../aspose.words/controlchar/tab) | Tab-tecken: "\x0009" eller "\t". |
| const [TabChar](../../aspose.words/controlchar/tabchar) | Tab-tecken: (char)9 eller "\t". |

### Anmärkningar

Ger både char- och strängversioner av samma konstanter. Till exempel: sträng ControlChar.LineBreak och char ControlChar.LineBreakChar har samma värde.

### Exempel

Visar hur man använder kontrolltecken.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga stycken med text med DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Konvertering av dokumentet till textform avslöjar att kontrolltecken
// representerar några av dokumentets strukturella element, såsom sidbrytningar.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// När du konverterar ett dokument till strängform,
// vi kan utelämna några av kontrolltecknen med Trim-metoden.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
