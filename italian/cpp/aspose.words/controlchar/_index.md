---
title: "Aspose::Words::ControlChar classe"
linktitle: "ControlChar"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ControlChar classe. Caratteri di controllo spesso incontrati nei documenti. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 18000
url: /it/cpp/aspose.words/controlchar/
---
## ControlChar class


Caratteri di controllo spesso incontrati nei documenti. Per saperne di più, visita l'articolo di documentazione [Working With Control Characters](https://docs.aspose.com/words/cpp/working-with-control-characters/).

```cpp
class ControlChar
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| static [Cell](./cell/)() | Carattere di fine cella di tabella o fine riga di tabella: "\x0007" o "\a". |
| static [ColumnBreak](./columnbreak/)() | Carattere di fine colonna: "\x000e". |
| [ControlChar](./controlchar/)() |  |
| static [Cr](./cr/)() | Carattere di ritorno a capo: "\x000d" o "\r". Uguale a [ParagraphBreak](./paragraphbreak/). |
| static [CrLf](./crlf/)() | Carattere di ritorno a capo seguito da avanzamento riga: "\x000d\x000a" o "\r\n". Non usato così nei documenti Microsoft Word, ma comunemente usato nei file di testo per interruzioni di paragrafo. |
| static [Lf](./lf/)() | Carattere di avanzamento riga: "\x000a" o "\n". Uguale a [LineFeed](./linefeed/). |
| static [LineBreak](./linebreak/)() | Carattere di interruzione di riga: "\x000b" o "\v". |
| static [LineFeed](./linefeed/)() | Carattere di avanzamento riga: "\x000a" o "\n". Uguale a [Lf](./lf/). |
| static [NonBreakingSpace](./nonbreakingspace/)() | Carattere di spazio non interrotto: "\x00a0". |
| static [PageBreak](./pagebreak/)() | Carattere di interruzione di pagina: "\x000c" o "\f". Nota che ha lo stesso valore di [SectionBreak](./sectionbreak/). |
| static [ParagraphBreak](./paragraphbreak/)() | Carattere di fine paragrafo: "\x000d" o "\r". Uguale a [Cr](./cr/) |
| static [SectionBreak](./sectionbreak/)() | Carattere di fine sezione: "\x000c" o "\f". Nota che ha lo stesso valore di [PageBreak](./pagebreak/). |
| static [Tab](./tab/)() | Carattere di tabulazione: "\x0009" o "\t". |
## Campi

| Campo | Descrizione |
| --- | --- |
| static constexpr [CellChar](./cellchar/) | Carattere di fine cella di tabella o fine riga di tabella: (char)7 o "\a". |
| static constexpr [ColumnBreakChar](./columnbreakchar/) | Carattere di fine colonna: (char)14. |
| static constexpr [DefaultTextInputChar](./defaulttextinputchar/) | Questo è il carattere "o" usato come valore predefinito nei campi di input di testo dei moduli. |
| static constexpr [FieldEndChar](./fieldendchar/) | Carattere di fine campo MS Word: (char)21. |
| static constexpr [FieldSeparatorChar](./fieldseparatorchar/) | Il carattere separatore di campo separa il codice del campo dal valore del campo. Opzionale in alcuni campi. Valore: (char)20. |
| static constexpr [FieldStartChar](./fieldstartchar/) | Carattere di inizio campo MS Word: (char)19. |
| static constexpr [LineBreakChar](./linebreakchar/) | Carattere di interruzione di riga: (char)11 o "\v". |
| static constexpr [LineFeedChar](./linefeedchar/) | Carattere di avanzamento riga: (char)10 o "\n". |
| static constexpr [NonBreakingHyphenChar](./nonbreakinghyphenchar/) | Il trattino non separabile in Microsoft Word è (char)30. |
| static constexpr [NonBreakingSpaceChar](./nonbreakingspacechar/) | Carattere di spazio non separabile: (char)160. |
| static constexpr [OptionalHyphenChar](./optionalhyphenchar/) | Il trattino opzionale in Microsoft Word è (char)31. |
| static constexpr [PageBreakChar](./pagebreakchar/) | Carattere di interruzione pagina: (char)12 o "\f". |
| static constexpr [ParagraphBreakChar](./paragraphbreakchar/) | Carattere di fine paragrafo: (char)13 o "\r". |
| static constexpr [SectionBreakChar](./sectionbreakchar/) | Carattere di fine sezione: (char)12 o "\f". |
| static constexpr [SpaceChar](./spacechar/) | Carattere spazio: (char)32. |
| static constexpr [TabChar](./tabchar/) | Carattere tabulazione: (char)9 o "\t". |

## Esempi



Mostra come utilizzare i caratteri di controllo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci paragrafi con testo usando DocumentBuilder.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Convertire il documento in forma testuale rivela che i caratteri di controllo
// rappresentano alcuni degli elementi strutturali del documento, come le interruzioni di pagina.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// Durante la conversione di un documento in forma stringa,
// possiamo omettere alcuni dei caratteri di controllo con il metodo Trim.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
