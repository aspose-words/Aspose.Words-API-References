---
title: ControlChar Class
linktitle: ControlChar
articleTitle: ControlChar
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.ControlChar för att effektivt hantera kontrolltecken i dina dokument för förbättrad formatering och läsbarhet.
type: docs
weight: 550
url: /sv/net/aspose.words/controlchar/
---
## ControlChar class

Kontrolltecken som ofta förekommer i dokument.

För att lära dig mer, besök[Arbeta med kontrolltecken](https://docs.aspose.com/words/net/working-with-control-characters/) dokumentationsartikel.

```csharp
public static class ControlChar
```

## Fält

| namn | Beskrivning |
| --- | --- |
| static readonly [Cell](../../aspose.words/controlchar/cell/) | Tecken för slutet av en tabellcell eller slutet av en tabellrad: "\x0007" eller "\a". |
| const [CellChar](../../aspose.words/controlchar/cellchar/) | Slutet av en tabellcell eller slutet av en tabellrad tecken: (char)7 eller "\a". |
| static readonly [ColumnBreak](../../aspose.words/controlchar/columnbreak/) | Slut på kolumntecken: "\x000e". |
| const [ColumnBreakChar](../../aspose.words/controlchar/columnbreakchar/) | Tecken i slutet av kolumnen: (char)14. |
| static readonly [Cr](../../aspose.words/controlchar/cr/) | Vagnreturtecken: "\x000d" eller "\r". Samma som[`ParagraphBreak`](./paragraphbreak/) . |
| static readonly [CrLf](../../aspose.words/controlchar/crlf/) | Vagnretur följt av radmatningstecken: "\x000d\x000a" eller "\r\n". Används inte som sådan i Microsoft Word-dokument, men används vanligtvis i textfiler för styckebrytningar. |
| const [DefaultTextInputChar](../../aspose.words/controlchar/defaulttextinputchar/) | Detta är tecknet "o" som används som standardvärde i textinmatningsfält. |
| const [FieldEndChar](../../aspose.words/controlchar/fieldendchar/) | Slut på MS Word-fälttecken: (char)21. |
| const [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) | Fältavgränsare separerar fältkod från fältvärde. Valfritt i vissa fält. Värde: (char)20. |
| const [FieldStartChar](../../aspose.words/controlchar/fieldstartchar/) | Början av MS Word-fälttecken: (char)19. |
| static readonly [Lf](../../aspose.words/controlchar/lf/) | Radmatningstecken: "\x000a" eller "\n". Samma som[`LineFeed`](./linefeed/) . |
| static readonly [LineBreak](../../aspose.words/controlchar/linebreak/) | Radbrytningstecken: "\x000b" eller "\v". |
| const [LineBreakChar](../../aspose.words/controlchar/linebreakchar/) | Radbrytningstecken: (char)11 eller "\v". |
| static readonly [LineFeed](../../aspose.words/controlchar/linefeed/) | Radmatningstecken: "\x000a" eller "\n". Samma som[`Lf`](./lf/) . |
| const [LineFeedChar](../../aspose.words/controlchar/linefeedchar/) | Radmatningstecken: (char)10 eller "\n". |
| const [NonBreakingHyphenChar](../../aspose.words/controlchar/nonbreakinghyphenchar/) | Hårdt bindestreck i Microsoft Word är (char)30. |
| static readonly [NonBreakingSpace](../../aspose.words/controlchar/nonbreakingspace/) | Hård mellanslagstecken: "\x00a0". |
| const [NonBreakingSpaceChar](../../aspose.words/controlchar/nonbreakingspacechar/) | Hård mellanslagstecken: (char)160. |
| const [OptionalHyphenChar](../../aspose.words/controlchar/optionalhyphenchar/) | Valfritt bindestreck i Microsoft Word är (char)31. |
| static readonly [PageBreak](../../aspose.words/controlchar/pagebreak/) | Sidbrytningstecken: "\x000c" eller "\f". Observera att det har samma värde som[`SectionBreak`](./sectionbreak/) . |
| const [PageBreakChar](../../aspose.words/controlchar/pagebreakchar/) | Sidbrytningstecken: (char)12 eller "\f". |
| static readonly [ParagraphBreak](../../aspose.words/controlchar/paragraphbreak/) | Sluttecken för stycke: "\x000d" eller "\r". Samma som[`Cr`](./cr/) |
| const [ParagraphBreakChar](../../aspose.words/controlchar/paragraphbreakchar/) | Sluttecken för stycke: (char)13 eller "\r". |
| static readonly [SectionBreak](../../aspose.words/controlchar/sectionbreak/) | Sluttecken för avsnitt: "\x000c" eller "\f". Observera att det har samma värde som[`PageBreak`](./pagebreak/) . |
| const [SectionBreakChar](../../aspose.words/controlchar/sectionbreakchar/) | Tecken för slutet av avsnittet: (char)12 eller "\f". |
| const [SpaceChar](../../aspose.words/controlchar/spacechar/) | Mellanslag: (char)32. |
| static readonly [Tab](../../aspose.words/controlchar/tab/) | Tabbtecken: "\x0009" eller "\t". |
| const [TabChar](../../aspose.words/controlchar/tabchar/) | Tab-tecken: (char)9 eller "\t". |

## Anmärkningar

Ger både tecken- och strängversioner av samma konstanter. Till exempel: sträng[`LineBreak`](./linebreak/) och char[`LineBreakChar`](./linebreakchar/) ha samma värde.

## Exempel

Visar hur man använder kontrolltecken.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga stycken med text med DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Att konvertera dokumentet till textformat visar att kontrolltecknen
// representerar några av dokumentets strukturella element, såsom sidbrytningar.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// När man konverterar ett dokument till strängformat,
// vi kan utelämna några av kontrolltecknen med Trim-metoden.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
