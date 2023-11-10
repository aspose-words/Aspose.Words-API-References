---
title: NumberStyle enumeration
linktitle: NumberStyle enumeration
articleTitle: NumberStyle enumeration
second_title: Aspose.Words for Python
description: "aspose.words.NumberStyle enumeration. Specifies the number style for a list, footnotes and endnotes, page numbers."
type: docs
weight: 790
url: /python-net/aspose.words/numberstyle/
---

## NumberStyle enumeration

Specifies the number style for a list, footnotes and endnotes, page numbers.


### Members

| Name | Description |
| --- | --- |
| ARABIC | Arabic numbering (1, 2, 3, ...) |
| UPPERCASE_ROMAN | Upper case Roman (I, II, III, ...) |
| LOWERCASE_ROMAN | Lower case Roman (i, ii, iii, ...) |
| UPPERCASE_LETTER | Upper case Letter (A, B, C, ...) |
| LOWERCASE_LETTER | Lower case letter (a, b, c, ...) |
| ORDINAL | Ordinal (1st, 2nd, 3rd, ...) |
| NUMBER | Numbered (One, Two, Three, ...) |
| ORDINAL_TEXT | Ordinal (text) (First, Second, Third, ...) |
| HEX | Hexadecimal: 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| CHICAGO_MANUAL | Chicago Manual of Style: \*, †, † |
| KANJI | Ideograph-digital |
| KANJI_DIGIT | Japanese counting |
| AIUEO_HALF_WIDTH | Aiueo |
| IROHA_HALF_WIDTH | Iroha |
| ARABIC_FULL_WIDTH | Full-width Arabic: 1, 2, 3, 4 |
| ARABIC_HALF_WIDTH | Half-width Arabic: 1, 2, 3, 4 |
| KANJI_TRADITIONAL | Japanese legal |
| KANJI_TRADITIONAL2 | Japanese digital ten thousand |
| NUMBER_IN_CIRCLE | Enclosed circles |
| DECIMAL_FULL_WIDTH | Decimal full width: 1, 2, 3, 4 |
| AIUEO | Aiueo full width |
| IROHA | Iroha full width |
| LEADING_ZERO | Leading Zero (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| BULLET | Bullet (check the character code in the text) |
| GANADA | Korean Ganada |
| CHOSUNG | Korea Chosung |
| GB1 | Enclosed full stop |
| GB2 | Enclosed parenthesis |
| GB3 | Enclosed circle Chinese |
| GB4 | Ideograph enclosed circle |
| ZODIAC1 | Ideograph traditional |
| ZODIAC2 | Ideograph Zodiac |
| ZODIAC3 | Ideograph Zodiac traditional |
| TRAD_CHIN_NUM1 | Taiwanese counting |
| TRAD_CHIN_NUM2 | Ideograph legal traditional |
| TRAD_CHIN_NUM3 | Taiwanese counting thousand |
| TRAD_CHIN_NUM4 | Taiwanese digital |
| SIMP_CHIN_NUM1 | Chinese counting |
| SIMP_CHIN_NUM2 | Chinese legal simplified |
| SIMP_CHIN_NUM3 | Chinese counting thousand |
| SIMP_CHIN_NUM4 | Chinese (not implemented) |
| HANJA_READ | Korean digital |
| HANJA_READ_DIGIT | Korean counting |
| HANGUL | Korea legal |
| HANJA | Korea digital2 |
| HEBREW1 | Hebrew-1 |
| ARABIC1 | Arabic alpha |
| HEBREW2 | Hebrew-2 |
| ARABIC2 | Arabic abjad |
| HINDI_LETTER1 | Hindi vowels |
| HINDI_LETTER2 | Hindi consonants |
| HINDI_ARABIC | Hindi numbers |
| HINDI_CARDINAL_TEXT | Hindi descriptive (cardinals) |
| THAI_LETTER | Thai letters |
| THAI_ARABIC | Thai numbers |
| THAI_CARDINAL_TEXT | Thai descriptive (cardinals) |
| VIET_CARDINAL_TEXT | Vietnamese descriptive (cardinals) |
| NUMBER_IN_DASH | Page number format: - 1 -, - 2 -, - 3 -, - 4 - |
| LOWERCASE_RUSSIAN | Lowercase Russian alphabet |
| UPPERCASE_RUSSIAN | Uppercase Russian alphabet |
| NONE | No bullet or number. |
| CUSTOM | Custom number format. It is supported by DOCX format only. |

### Examples

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```python
doc = aw.Document()

# A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
# We can create nested lists by increasing the indent level.
# We can begin and end a list by using a document builder's "list_format" property.
# Each paragraph that we add between a list's start and the end will become an item in the list.
# Create a list from a Microsoft Word template, and customize the first two of its list levels.
list = doc.lists.add(aw.lists.ListTemplate.NUMBER_DEFAULT)

list_level = list.list_levels[0]
list_level.font.color = drawing.Color.red
list_level.font.size = 24
list_level.number_style = aw.NumberStyle.ORDINAL_TEXT
list_level.start_at = 21
list_level.number_format = "\u0000"

list_level.number_position = -36
list_level.text_position = 144
list_level.tab_position = 144

list_level = list.list_levels[1]
list_level.alignment = aw.lists.ListLevelAlignment.RIGHT
list_level.number_style = aw.NumberStyle.BULLET
list_level.font.name = "Wingdings"
list_level.font.color = drawing.Color.blue
list_level.font.size = 24

# This NumberFormat value will create star-shaped bullet list symbols.
list_level.number_format = "\uf0af"
list_level.trailing_character = aw.lists.ListTrailingCharacter.SPACE
list_level.number_position = 144

# Create paragraphs and apply both list levels of our custom list formatting to them.
builder = aw.DocumentBuilder(doc)

builder.list_format.list = list
builder.writeln("The quick brown fox...")
builder.writeln("The quick brown fox...")

builder.list_format.list_indent()
builder.writeln("jumped over the lazy dog.")
builder.writeln("jumped over the lazy dog.")

builder.list_format.list_outdent()
builder.writeln("The quick brown fox...")

builder.list_format.remove_numbers()

builder.document.save(ARTIFACTS_DIR + "Lists.create_custom_list.docx")
```

### See Also

* module [aspose.words](../)

