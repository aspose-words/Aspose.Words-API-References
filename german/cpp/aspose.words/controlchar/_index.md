---
title: "Aspose::Words::ControlChar class"
linktitle: "ControlChar"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ControlChar class. Steuerzeichen, die häufig in Dokumenten vorkommen. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 18000
url: /de/cpp/aspose.words/controlchar/
---
## ControlChar class


Steuerzeichen, die häufig in Dokumenten vorkommen. Weitere Informationen finden Sie im Dokumentationsartikel [Working With Control Characters](https://docs.aspose.com/words/cpp/working-with-control-characters/).

```cpp
class ControlChar
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| static [Cell](./cell/)() | Ende eines Tabellenzellen- oder Tabellenzeilenzeichens: "\x0007" oder "\a". |
| static [ColumnBreak](./columnbreak/)() | Ende des Spaltenzeichens: "\x000e". |
| [ControlChar](./controlchar/)() |  |
| static [Cr](./cr/)() | Wagenrücklaufzeichen: "\x000d" oder "\r". Gleich wie [ParagraphBreak](./paragraphbreak/). |
| static [CrLf](./crlf/)() | Wagenrücklauf gefolgt von Zeilenumbruchzeichen: "\x000d\x000a" oder "\r\n". Wird in Microsoft‑Word‑Dokumenten nicht so verwendet, ist aber in Textdateien für Absatzumbrüche üblich. |
| static [Lf](./lf/)() | Zeilenumbruchzeichen: "\x000a" oder "\n". Gleich wie [LineFeed](./linefeed/). |
| static [LineBreak](./linebreak/)() | Zeilenumbruchzeichen: "\x000b" oder "\v". |
| static [LineFeed](./linefeed/)() | Zeilenumbruchzeichen: "\x000a" oder "\n". Gleich wie [Lf](./lf/). |
| static [NonBreakingSpace](./nonbreakingspace/)() | Geschütztes Leerzeichen: "\x00a0". |
| static [PageBreak](./pagebreak/)() | Seitenumbruchzeichen: "\x000c" oder "\f". Hinweis: Es hat denselben Wert wie [SectionBreak](./sectionbreak/). |
| static [ParagraphBreak](./paragraphbreak/)() | Absatzendezeichen: "\x000d" oder "\r". Gleich wie [Cr](./cr/) |
| static [SectionBreak](./sectionbreak/)() | Abschnittsendezeichen: "\x000c" oder "\f". Hinweis: Es hat denselben Wert wie [PageBreak](./pagebreak/). |
| static [Tab](./tab/)() | Tabulatorzeichen: "\x0009" oder "\t". |
## Felder

| Feld | Beschreibung |
| --- | --- |
| static constexpr [CellChar](./cellchar/) | Ende eines Tabellenzellen- oder Tabellenzeilenzeichens: (char)7 oder "\a". |
| static constexpr [ColumnBreakChar](./columnbreakchar/) | Ende des Spaltenzeichens: (char)14. |
| static constexpr [DefaultTextInputChar](./defaulttextinputchar/) | Dies ist das Zeichen "o", das als Standardwert in Texteingabeformularfeldern verwendet wird. |
| static constexpr [FieldEndChar](./fieldendchar/) | Ende des MS‑Word‑Feldzeichens: (char)21. |
| static constexpr [FieldSeparatorChar](./fieldseparatorchar/) | Das Feldtrennzeichen trennt den Feldcode vom Feldwert. Optional in einigen Feldern. Wert: (char)20. |
| static constexpr [FieldStartChar](./fieldstartchar/) | Startzeichen für ein MS‑Word‑Feld: (char)19. |
| static constexpr [LineBreakChar](./linebreakchar/) | Zeilenumbruchzeichen: (char)11 oder "\v". |
| static constexpr [LineFeedChar](./linefeedchar/) | Zeilenumlaufzeichen: (char)10 oder "\n". |
| static constexpr [NonBreakingHyphenChar](./nonbreakinghyphenchar/) | Das geschützte Bindestrich‑Zeichen in Microsoft Word ist (char)30. |
| static constexpr [NonBreakingSpaceChar](./nonbreakingspacechar/) | Geschütztes Leerzeichen: (char)160. |
| static constexpr [OptionalHyphenChar](./optionalhyphenchar/) | Optionales Bindestrich‑Zeichen in Microsoft Word ist (char)31. |
| static constexpr [PageBreakChar](./pagebreakchar/) | Seitenumbruchzeichen: (char)12 oder "\f". |
| static constexpr [ParagraphBreakChar](./paragraphbreakchar/) | Absatzendezeichen: (char)13 oder "\r". |
| static constexpr [SectionBreakChar](./sectionbreakchar/) | Abschnittsendezeichen: (char)12 oder "\f". |
| static constexpr [SpaceChar](./spacechar/) | Leerzeichen: (char)32. |
| static constexpr [TabChar](./tabchar/) | Tabulatorzeichen: (char)9 oder "\t". |

## Beispiele



Zeigt, wie Steuerzeichen verwendet werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügt Absätze mit Text mittels DocumentBuilder ein.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Das Konvertieren des Dokuments in Textform zeigt, dass Steuerzeichen
// einige der strukturellen Elemente des Dokuments darstellen, wie z. B. Seitenumbrüche.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// Beim Konvertieren eines Dokuments in Zeichenkettenform,
// können wir einige Steuerzeichen mit der Trim-Methode weglassen.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
