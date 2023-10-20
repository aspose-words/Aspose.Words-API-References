---
title: ControlChar Class
linktitle: ControlChar
articleTitle: ControlChar
second_title: Aspose.Words per .NET
description: Aspose.Words.ControlChar classe. Caratteri di controllo spesso incontrati nei documenti in C#.
type: docs
weight: 350
url: /it/net/aspose.words/controlchar/
---
## ControlChar class

Caratteri di controllo spesso incontrati nei documenti.

Per saperne di più, visita il[Lavorare con i caratteri di controllo](https://docs.aspose.com/words/net/working-with-control-characters/) articolo di documentazione.

```csharp
public static class ControlChar
```

## Campi

| Nome | Descrizione |
| --- | --- |
| static readonly [Cell](../../aspose.words/controlchar/cell/) | Fine della cella della tabella o fine della riga della tabella. Carattere: "\x0007" o "\a". |
| const [CellChar](../../aspose.words/controlchar/cellchar/) | Fine di una cella di tabella o fine di una riga di tabella carattere: (char)7 o "\a". |
| static readonly [ColumnBreak](../../aspose.words/controlchar/columnbreak/) | Carattere di fine colonna: "\x000e". |
| const [ColumnBreakChar](../../aspose.words/controlchar/columnbreakchar/) | Carattere di fine colonna: (char)14. |
| static readonly [Cr](../../aspose.words/controlchar/cr/) | Carattere di ritorno a capo: "\x000d" o "\r". Uguale a[`ParagraphBreak`](./paragraphbreak/) . |
| static readonly [CrLf](../../aspose.words/controlchar/crlf/) | Ritorno a capo seguito dal carattere di avanzamento riga: "\x000d\x000a" o "\r\n". Non utilizzato come tale nei documenti Microsoft Word, ma comunemente utilizzato nei file di testo per le interruzioni di paragrafo. |
| const [DefaultTextInputChar](../../aspose.words/controlchar/defaulttextinputchar/) | Questo è il carattere "o" utilizzato come valore predefinito nei campi del modulo di immissione testo. |
| const [FieldEndChar](../../aspose.words/controlchar/fieldendchar/) | Fine del carattere del campo MS Word: (char)21. |
| const [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) | Il carattere separatore di campo separa il codice di campo dal valore del campo. Facoltativo in alcuni campi. Valore: (carattere)20. |
| const [FieldStartChar](../../aspose.words/controlchar/fieldstartchar/) | Carattere iniziale del campo MS Word: (char)19. |
| static readonly [Lf](../../aspose.words/controlchar/lf/) | Carattere di avanzamento riga: "\x000a" o "\n". Uguale a[`LineFeed`](./linefeed/) . |
| static readonly [LineBreak](../../aspose.words/controlchar/linebreak/) | Carattere di interruzione di riga: "\x000b" o "\v". |
| const [LineBreakChar](../../aspose.words/controlchar/linebreakchar/) | Carattere di interruzione di riga: (char)11 o "\v". |
| static readonly [LineFeed](../../aspose.words/controlchar/linefeed/) | Carattere di avanzamento riga: "\x000a" o "\n". Uguale a[`Lf`](./lf/) . |
| const [LineFeedChar](../../aspose.words/controlchar/linefeedchar/) | Carattere di avanzamento riga: (carattere)10 o "\n". |
| const [NonBreakingHyphenChar](../../aspose.words/controlchar/nonbreakinghyphenchar/) | Il trattino unificatore in Microsoft Word è (char)30. |
| static readonly [NonBreakingSpace](../../aspose.words/controlchar/nonbreakingspace/) | Spazio unificatore: "\x00a0". |
| const [NonBreakingSpaceChar](../../aspose.words/controlchar/nonbreakingspacechar/) | Spazio unificatore: (char)160. |
| const [OptionalHyphenChar](../../aspose.words/controlchar/optionalhyphenchar/) | Il trattino facoltativo in Microsoft Word è (char)31. |
| static readonly [PageBreak](../../aspose.words/controlchar/pagebreak/) | Carattere di interruzione di pagina: "\x000c" o "\f". Nota che ha lo stesso valore di[`SectionBreak`](./sectionbreak/) . |
| const [PageBreakChar](../../aspose.words/controlchar/pagebreakchar/) | Carattere di interruzione di pagina: (char)12 o "\f". |
| static readonly [ParagraphBreak](../../aspose.words/controlchar/paragraphbreak/) | Carattere di fine paragrafo: "\x000d" o "\r". Uguale a[`Cr`](./cr/) |
| const [ParagraphBreakChar](../../aspose.words/controlchar/paragraphbreakchar/) | Carattere di fine paragrafo: (char)13 o "\r". |
| static readonly [SectionBreak](../../aspose.words/controlchar/sectionbreak/) | Carattere di fine sezione: "\x000c" o "\f". Nota che ha lo stesso valore di[`PageBreak`](./pagebreak/) . |
| const [SectionBreakChar](../../aspose.words/controlchar/sectionbreakchar/) | Carattere di fine sezione: (char)12 oppure "\f". |
| const [SpaceChar](../../aspose.words/controlchar/spacechar/) | Spazio: (carattere)32. |
| static readonly [Tab](../../aspose.words/controlchar/tab/) | Carattere di tabulazione: "\x0009" o "\t". |
| const [TabChar](../../aspose.words/controlchar/tabchar/) | Carattere di tabulazione: (char)9 o "\t". |

## Osservazioni

Fornisce versioni sia di carattere che di stringa delle stesse costanti. Ad esempio: stringa[`LineBreak`](./linebreak/) e salmerino[`LineBreakChar`](./linebreakchar/) hanno lo stesso valore.

## Esempi

Mostra come utilizzare i caratteri di controllo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci paragrafi con testo con DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// La conversione del documento in formato testo rivela i caratteri di controllo
// rappresenta alcuni degli elementi strutturali del documento, come le interruzioni di pagina.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Quando si converte un documento in formato stringa,
// possiamo omettere alcuni caratteri di controllo con il metodo Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
