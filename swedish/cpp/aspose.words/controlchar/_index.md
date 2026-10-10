---
title: "Aspose::Words::ControlChar class"
linktitle: "ControlChar"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ControlChar class. Kontrolltecken som ofta förekommer i dokument. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 18000
url: /sv/cpp/aspose.words/controlchar/
---
## ControlChar class


Kontrolltecken som ofta förekommer i dokument. För att läsa mer, besök dokumentationsartikeln [Arbeta med kontrolltecken](https://docs.aspose.com/words/cpp/working-with-control-characters/).

```cpp
class ControlChar
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| static [Cell](./cell/)() | Tecken för slutet av en tabellcell eller slutet av en tabellrad: "\x0007" eller "\a". |
| static [ColumnBreak](./columnbreak/)() | Tecken för slutet av en kolumn: "\x000e". |
| [ControlChar](./controlchar/)() |  |
| static [Cr](./cr/)() | Vagnreturtecken: "\x000d" eller "\r". Samma som [ParagraphBreak](./paragraphbreak/). |
| static [CrLf](./crlf/)() | Vagnretur följt av radmatningstecken: "\x000d\x000a" eller "\r\n". Används inte på detta sätt i Microsoft Word-dokument, men är vanligt i textfiler för styckebrytningar. |
| static [Lf](./lf/)() | Radmatningstecken: "\x000a" eller "\n". Samma som [LineFeed](./linefeed/). |
| static [LineBreak](./linebreak/)() | Radbrytningstecken: "\x000b" eller "\v". |
| static [LineFeed](./linefeed/)() | Radmatningstecken: "\x000a" eller "\n". Samma som [Lf](./lf/). |
| static [NonBreakingSpace](./nonbreakingspace/)() | Icke-brytande mellanslagstecken: "\x00a0". |
| static [PageBreak](./pagebreak/)() | Sidbrytningstecken: "\x000c" eller "\f". Observera att det har samma värde som [SectionBreak](./sectionbreak/). |
| static [ParagraphBreak](./paragraphbreak/)() | Tecken för slutet av ett stycke: "\x000d" eller "\r". Samma som [Cr](./cr/) |
| static [SectionBreak](./sectionbreak/)() | Tecken för slutet av ett avsnitt: "\x000c" eller "\f". Observera att det har samma värde som [PageBreak](./pagebreak/). |
| static [Tab](./tab/)() | Tabulatortecken: "\x0009" eller "\t". |
## Fält

| Fält | Beskrivning |
| --- | --- |
| static constexpr [CellChar](./cellchar/) | Tecken för slutet av en tabellcell eller slutet av en tabellrad: (char)7 eller "\a". |
| static constexpr [ColumnBreakChar](./columnbreakchar/) | Tecken för slutet av en kolumn: (char)14. |
| static constexpr [DefaultTextInputChar](./defaulttextinputchar/) | Detta är "o"-tecknet som används som standardvärde i textinmatningsfält i formulär. |
| static constexpr [FieldEndChar](./fieldendchar/) | Tecken för slutet av ett MS Word-fält: (char)21. |
| static constexpr [FieldSeparatorChar](./fieldseparatorchar/) | Fältseparatorstecknet separerar fältkod från fältvärde. Valfritt i vissa fält. Värde: (char)20. |
| static constexpr [FieldStartChar](./fieldstartchar/) | Start av MS Word-fälttecken: (char)19. |
| static constexpr [LineBreakChar](./linebreakchar/) | Radbrytningstecken: (char)11 eller "\\v". |
| static constexpr [LineFeedChar](./linefeedchar/) | Radmatningstecken: (char)10 eller "\\n". |
| static constexpr [NonBreakingHyphenChar](./nonbreakinghyphenchar/) | Icke-brytande bindestreck i Microsoft Word är (char)30. |
| static constexpr [NonBreakingSpaceChar](./nonbreakingspacechar/) | Icke-brytande mellanslagstecken: (char)160. |
| static constexpr [OptionalHyphenChar](./optionalhyphenchar/) | Valfritt bindestreck i Microsoft Word är (char)31. |
| static constexpr [PageBreakChar](./pagebreakchar/) | Sidbrytningstecken: (char)12 eller "\\f". |
| static constexpr [ParagraphBreakChar](./paragraphbreakchar/) | Tecken för styckeslut: (char)13 eller "\\r". |
| static constexpr [SectionBreakChar](./sectionbreakchar/) | Tecken för avsnittsslut: (char)12 eller "\\f". |
| static constexpr [SpaceChar](./spacechar/) | Mellanslagstecken: (char)32. |
| static constexpr [TabChar](./tabchar/) | Tabulatortecken: (char)9 eller "\\t". |

## Exempel



Visar hur man använder kontrolltecken.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga stycken med text med DocumentBuilder.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Att konvertera dokumentet till textform avslöjar att kontrolltecken
// representerar några av dokumentets strukturella element, såsom sidbrytningar.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// När man konverterar ett dokument till strängform,
// kan vi utelämna vissa kontrolltecken med Trim‑metoden.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
