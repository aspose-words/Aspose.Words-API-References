---
title: Class ControlChar
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.ControlChar klas. Steuerzeichen die häufig in Dokumenten vorkommen.
type: docs
weight: 340
url: /de/net/aspose.words/controlchar/
---
## ControlChar class

Steuerzeichen, die häufig in Dokumenten vorkommen.

```csharp
public static class ControlChar
```

## Felder

| Name | Beschreibung |
| --- | --- |
| static readonly [Cell](../../aspose.words/controlchar/cell/) | Ende einer Tabellenzelle oder Ende einer Tabellenzeile Zeichen: "\x0007" oder "\a". |
| const [CellChar](../../aspose.words/controlchar/cellchar/) | Ende einer Tabellenzelle oder Ende einer Tabellenzeile Zeichen: (char)7 oder "\a". |
| static readonly [ColumnBreak](../../aspose.words/controlchar/columnbreak/) | Spaltenendezeichen: "\x000e". |
| const [ColumnBreakChar](../../aspose.words/controlchar/columnbreakchar/) | Spaltenendezeichen: (char)14. |
| static readonly [Cr](../../aspose.words/controlchar/cr/) | Wagenrücklaufzeichen: "\x000d" oder "\r". Gleich wie[`ParagraphBreak`](./paragraphbreak/) . |
| static readonly [CrLf](../../aspose.words/controlchar/crlf/) | Wagenrücklauf gefolgt von Zeilenvorschubzeichen: "\x000d\x000a" oder "\r\n". Nicht als solches in Microsoft Word-Dokumenten verwendet, aber häufig in Textdateien für Absatzumbrüche verwendet. |
| const [DefaultTextInputChar](../../aspose.words/controlchar/defaulttextinputchar/) | Dies ist das Zeichen „o“, das als Standardwert in Texteingabeformularfeldern verwendet wird. |
| const [FieldEndChar](../../aspose.words/controlchar/fieldendchar/) | Ende des MS-Word-Feldzeichens: (char)21. |
| const [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) | Feldtrennzeichen trennt Feldcode vom Feldwert. Optional in einigen Feldern. Wert: (Zeichen)20. |
| const [FieldStartChar](../../aspose.words/controlchar/fieldstartchar/) | Beginn des MS-Word-Feldzeichens: (char)19. |
| static readonly [Lf](../../aspose.words/controlchar/lf/) | Zeilenvorschubzeichen: "\x000a" oder "\n". Gleich wie[`LineFeed`](./linefeed/) . |
| static readonly [LineBreak](../../aspose.words/controlchar/linebreak/) | Zeilenumbruchzeichen: "\x000b" oder "\v". |
| const [LineBreakChar](../../aspose.words/controlchar/linebreakchar/) | Zeilenumbruchzeichen: (char)11 oder "\v". |
| static readonly [LineFeed](../../aspose.words/controlchar/linefeed/) | Zeilenvorschubzeichen: "\x000a" oder "\n". Gleich wie[`Lf`](./lf/) . |
| const [LineFeedChar](../../aspose.words/controlchar/linefeedchar/) | Zeilenvorschubzeichen: (char)10 oder "\n". |
| const [NonBreakingHyphenChar](../../aspose.words/controlchar/nonbreakinghyphenchar/) | Geschützter Bindestrich in Microsoft Word ist (char)30. |
| static readonly [NonBreakingSpace](../../aspose.words/controlchar/nonbreakingspace/) | Geschütztes Leerzeichen: "\x00a0". |
| const [NonBreakingSpaceChar](../../aspose.words/controlchar/nonbreakingspacechar/) | Geschütztes Leerzeichen: (char)160. |
| const [OptionalHyphenChar](../../aspose.words/controlchar/optionalhyphenchar/) | Optionaler Bindestrich in Microsoft Word ist (char)31. |
| static readonly [PageBreak](../../aspose.words/controlchar/pagebreak/) | Seitenumbruchzeichen: "\x000c" oder "\f". Beachten Sie, dass es denselben Wert hat wie[`SectionBreak`](./sectionbreak/) . |
| const [PageBreakChar](../../aspose.words/controlchar/pagebreakchar/) | Seitenumbruchzeichen: (char)12 oder "\f". |
| static readonly [ParagraphBreak](../../aspose.words/controlchar/paragraphbreak/) | Absatzendezeichen: "\x000d" oder "\r". Gleich wie[`Cr`](./cr/) |
| const [ParagraphBreakChar](../../aspose.words/controlchar/paragraphbreakchar/) | Absatzendezeichen: (char)13 oder "\r". |
| static readonly [SectionBreak](../../aspose.words/controlchar/sectionbreak/) | Abschnittsendezeichen: "\x000c" oder "\f". Beachten Sie, dass es denselben Wert hat wie[`PageBreak`](./pagebreak/) . |
| const [SectionBreakChar](../../aspose.words/controlchar/sectionbreakchar/) | Abschnittsendezeichen: (char)12 oder "\f". |
| const [SpaceChar](../../aspose.words/controlchar/spacechar/) | Leerzeichen: (char)32. |
| static readonly [Tab](../../aspose.words/controlchar/tab/) | Tabulatorzeichen: "\x0009" oder "\t". |
| const [TabChar](../../aspose.words/controlchar/tabchar/) | Tabulatorzeichen: (char)9 oder "\t". |

### Bemerkungen

Stellt sowohl Char- als auch String-Versionen derselben Konstanten bereit. Beispiel: string ControlChar.LineBreak und char ControlChar.LineBreakChar haben denselben Wert.

### Beispiele

Zeigt, wie Steuerzeichen verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Absätze mit Text mit DocumentBuilder einfügen.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Das Konvertieren des Dokuments in Textform zeigt diese Steuerzeichen
// stellen einige der Strukturelemente des Dokuments dar, wie z. B. Seitenumbrüche.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Beim Konvertieren eines Dokuments in eine Zeichenkette,
// Mit der Trim-Methode können wir einige der Steuerzeichen weglassen.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


