---
title: ControlChar Class
linktitle: ControlChar
articleTitle: ControlChar
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.ControlChar, um Steuerzeichen in Ihren Dokumenten effektiv zu verwalten und so die Formatierung und Lesbarkeit zu verbessern.
type: docs
weight: 550
url: /de/net/aspose.words/controlchar/
---
## ControlChar class

In Dokumenten häufig vorkommende Steuerzeichen.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Steuerzeichen](https://docs.aspose.com/words/net/working-with-control-characters/) Dokumentationsartikel.

```csharp
public static class ControlChar
```

## Felder

| Name | Beschreibung |
| --- | --- |
| static readonly [Cell](../../aspose.words/controlchar/cell/) | Zeichen für das Ende einer Tabellenzelle oder das Ende einer Tabellenzeile: "\x0007" oder "\a". |
| const [CellChar](../../aspose.words/controlchar/cellchar/) | Ende einer Tabellenzelle oder Ende einer Tabellenzeile Zeichen: (char)7 oder "\a". |
| static readonly [ColumnBreak](../../aspose.words/controlchar/columnbreak/) | Spaltenendezeichen: "\x000e". |
| const [ColumnBreakChar](../../aspose.words/controlchar/columnbreakchar/) | Spaltenendezeichen: (char)14. |
| static readonly [Cr](../../aspose.words/controlchar/cr/) | Wagenrücklaufzeichen: "\x000d" oder "\r". Dasselbe wie[`ParagraphBreak`](./paragraphbreak/) . |
| static readonly [CrLf](../../aspose.words/controlchar/crlf/) | Wagenrücklauf gefolgt von einem Zeilenvorschubzeichen: "\x000d\x000a" oder "\r\n". Wird als solches in Microsoft Word-Dokumenten nicht verwendet, wird aber häufig in Textdateien für Absatzumbrüche verwendet. |
| const [DefaultTextInputChar](../../aspose.words/controlchar/defaulttextinputchar/) | Dies ist das Zeichen „o“, das als Standardwert in Texteingabeformularfeldern verwendet wird. |
| const [FieldEndChar](../../aspose.words/controlchar/fieldendchar/) | Ende des MS Word-Feldzeichens: (char)21. |
| const [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) | Das Feldtrennzeichen trennt den Feldcode vom Feldwert. In einigen Feldern optional. Wert: (char)20. |
| const [FieldStartChar](../../aspose.words/controlchar/fieldstartchar/) | Beginn des MS Word-Feldzeichens: (char)19. |
| static readonly [Lf](../../aspose.words/controlchar/lf/) | Zeilenvorschubzeichen: "\x000a" oder "\n". Dasselbe wie[`LineFeed`](./linefeed/) . |
| static readonly [LineBreak](../../aspose.words/controlchar/linebreak/) | Zeilenumbruchzeichen: "\x000b" oder "\v". |
| const [LineBreakChar](../../aspose.words/controlchar/linebreakchar/) | Zeilenumbruchzeichen: (char)11 oder "\v". |
| static readonly [LineFeed](../../aspose.words/controlchar/linefeed/) | Zeilenvorschubzeichen: "\x000a" oder "\n". Dasselbe wie[`Lf`](./lf/) . |
| const [LineFeedChar](../../aspose.words/controlchar/linefeedchar/) | Zeilenvorschubzeichen: (char)10 oder "\n". |
| const [NonBreakingHyphenChar](../../aspose.words/controlchar/nonbreakinghyphenchar/) | Geschützter Bindestrich in Microsoft Word ist (char)30. |
| static readonly [NonBreakingSpace](../../aspose.words/controlchar/nonbreakingspace/) | Geschütztes Leerzeichen: "\x00a0". |
| const [NonBreakingSpaceChar](../../aspose.words/controlchar/nonbreakingspacechar/) | Geschütztes Leerzeichen: (char)160. |
| const [OptionalHyphenChar](../../aspose.words/controlchar/optionalhyphenchar/) | Optionaler Bindestrich in Microsoft Word ist (char)31. |
| static readonly [PageBreak](../../aspose.words/controlchar/pagebreak/) | Seitenumbruchzeichen: "\x000c" oder "\f". Beachten Sie, dass es den gleichen Wert hat wie[`SectionBreak`](./sectionbreak/) . |
| const [PageBreakChar](../../aspose.words/controlchar/pagebreakchar/) | Seitenumbruchzeichen: (char)12 oder "\f". |
| static readonly [ParagraphBreak](../../aspose.words/controlchar/paragraphbreak/) | Absatzendezeichen: "\x000d" oder "\r". Dasselbe wie[`Cr`](./cr/) |
| const [ParagraphBreakChar](../../aspose.words/controlchar/paragraphbreakchar/) | Absatzendezeichen: (char)13 oder "\r". |
| static readonly [SectionBreak](../../aspose.words/controlchar/sectionbreak/) | Abschnittsendezeichen: "\x000c" oder "\f". Beachten Sie, dass es den gleichen Wert hat wie[`PageBreak`](./pagebreak/) . |
| const [SectionBreakChar](../../aspose.words/controlchar/sectionbreakchar/) | Abschnittsendezeichen: (char)12 oder "\f". |
| const [SpaceChar](../../aspose.words/controlchar/spacechar/) | Leerzeichen: (char)32. |
| static readonly [Tab](../../aspose.words/controlchar/tab/) | Tabulatorzeichen: "\x0009" oder "\t". |
| const [TabChar](../../aspose.words/controlchar/tabchar/) | Tabulatorzeichen: (char)9 oder "\t". |

## Bemerkungen

Bietet sowohl Char- als auch String-Versionen derselben Konstanten. Beispiel: string[`LineBreak`](./linebreak/) und Saibling[`LineBreakChar`](./linebreakchar/) haben den gleichen Wert.

## Beispiele

Zeigt, wie Steuerzeichen verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie mit DocumentBuilder Absätze mit Text ein.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Die Konvertierung des Dokuments in Textform zeigt, dass Steuerzeichen
// stellen einige Strukturelemente des Dokuments dar, beispielsweise Seitenumbrüche.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Beim Konvertieren eines Dokuments in die Zeichenfolgenform,
// Wir können einige der Steuerzeichen mit der Trim-Methode weglassen.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
