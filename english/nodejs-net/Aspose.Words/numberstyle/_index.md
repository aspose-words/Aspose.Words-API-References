---
title: NumberStyle enumeration
linktitle: NumberStyle enumeration
articleTitle: NumberStyle enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.NumberStyle enumeration. Specifies the number style for a list, footnotes and endnotes, page numbers."
type: docs
weight: 910
url: /nodejs-net/Aspose.Words/numberstyle/
---

## NumberStyle enumeration

Specifies the number style for a list, footnotes and endnotes, page numbers.


### Members

| Name | Description |
| --- | --- |
| Arabic | Arabic numbering (1, 2, 3, ...) |
| UppercaseRoman | Upper case Roman (I, II, III, ...) |
| LowercaseRoman | Lower case Roman (i, ii, iii, ...) |
| UppercaseLetter | Upper case Letter (A, B, C, ...) |
| LowercaseLetter | Lower case letter (a, b, c, ...) |
| Ordinal | Ordinal (1st, 2nd, 3rd, ...) |
| Number | Numbered (One, Two, Three, ...) |
| OrdinalText | Ordinal (text) (First, Second, Third, ...) |
| Hex | Hexadecimal: 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| ChicagoManual | Chicago Manual of Style: \*, †, † |
| Kanji | Ideograph-digital |
| KanjiDigit | Japanese counting |
| AiueoHalfWidth | Aiueo |
| IrohaHalfWidth | Iroha |
| ArabicFullWidth | Full-width Arabic: 1, 2, 3, 4 |
| ArabicHalfWidth | Half-width Arabic: 1, 2, 3, 4 |
| KanjiTraditional | Japanese legal |
| KanjiTraditional2 | Japanese digital ten thousand |
| NumberInCircle | Enclosed circles |
| DecimalFullWidth | Decimal full width: 1, 2, 3, 4 |
| Aiueo | Aiueo full width |
| Iroha | Iroha full width |
| LeadingZero | Leading Zero (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | Bullet (check the character code in the text) |
| Ganada | Korean Ganada |
| Chosung | Korea Chosung |
| GB1 | Enclosed full stop |
| GB2 | Enclosed parenthesis |
| GB3 | Enclosed circle Chinese |
| GB4 | Ideograph enclosed circle |
| Zodiac1 | Ideograph traditional |
| Zodiac2 | Ideograph Zodiac |
| Zodiac3 | Ideograph Zodiac traditional |
| TradChinNum1 | Taiwanese counting |
| TradChinNum2 | Ideograph legal traditional |
| TradChinNum3 | Taiwanese counting thousand |
| TradChinNum4 | Taiwanese digital |
| SimpChinNum1 | Chinese counting |
| SimpChinNum2 | Chinese legal simplified |
| SimpChinNum3 | Chinese counting thousand |
| SimpChinNum4 | Chinese (not implemented) |
| HanjaRead | Korean digital |
| HanjaReadDigit | Korean counting |
| Hangul | Korea legal |
| Hanja | Korea digital2 |
| Hebrew1 | Hebrew-1 |
| Arabic1 | Arabic alpha |
| Hebrew2 | Hebrew-2 |
| Arabic2 | Arabic abjad |
| HindiLetter1 | Hindi vowels |
| HindiLetter2 | Hindi consonants |
| HindiArabic | Hindi numbers |
| HindiCardinalText | Hindi descriptive (cardinals) |
| ThaiLetter | Thai letters |
| ThaiArabic | Thai numbers |
| ThaiCardinalText | Thai descriptive (cardinals) |
| VietCardinalText | Vietnamese descriptive (cardinals) |
| NumberInDash | Page number format: - 1 -, - 2 -, - 3 -, - 4 - |
| LowercaseRussian | Lowercase Russian alphabet |
| UppercaseRussian | Uppercase Russian alphabet |
| None | No bullet or number. |
| Custom | Custom number format. It is supported by DOCX format only. |

### Examples

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```js
let doc = new aw.Document();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Create a list from a Microsoft Word template, and customize the first two of its list levels.
let list = doc.lists.add(aw.Lists.ListTemplate.NumberDefault);

let listLevel = list.listLevels.at(0);
listLevel.font.color = "#FF0000";
listLevel.font.size = 24;
listLevel.numberStyle = aw.NumberStyle.OrdinalText;
listLevel.startAt = 21;
listLevel.numberFormat = "\u0000";

listLevel.numberPosition = -36;
listLevel.textPosition = 144;
listLevel.tabPosition = 144;

listLevel = list.listLevels.at(1);
listLevel.alignment = aw.Lists.ListLevelAlignment.Right;
listLevel.numberStyle = aw.NumberStyle.Bullet;
listLevel.font.name = "Wingdings";
listLevel.font.color = "#0000FF";
listLevel.font.size = 24;

// This NumberFormat value will create star-shaped bullet list symbols.
listLevel.numberFormat = "\uf0af";
listLevel.trailingCharacter = aw.Lists.ListTrailingCharacter.Space;
listLevel.numberPosition = 144;

// Create paragraphs and apply both list levels of our custom list formatting to them.
let builder = new aw.DocumentBuilder(doc);

builder.listFormat.list = list;
builder.writeln("The quick brown fox...");
builder.writeln("The quick brown fox...");

builder.listFormat.listIndent();
builder.writeln("jumped over the lazy dog.");
builder.writeln("jumped over the lazy dog.");

builder.listFormat.listOutdent();
builder.writeln("The quick brown fox...");

builder.listFormat.removeNumbers();

builder.document.save(base.artifactsDir + "Lists.CreateCustomList.docx");
```

### See Also

* module [Aspose.Words](../)

