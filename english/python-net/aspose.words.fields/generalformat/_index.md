---
title: GeneralFormat enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies a general format that is applied to a numeric, text, or any field result"
type: docs
weight: 1180
url: /python-net/aspose.words.fields/generalformat/
---

## GeneralFormat enumeration

Specifies a general format that is applied to a numeric, text, or any field result.
A field may have a combination of general formats.


### Members

| Name | Description |
| --- | --- |
| NONE | Used to specify a missing general format. |
| AIUEO | Numeric formatting. Formats a numeric result using hiragana characters in the traditional a-i-u-e-o order. |
| UPPERCASE_ALPHABETIC | Numeric formatting. Formats a numeric result as one or more occurrences of an uppercase alphabetic Latin character. |
| LOWERCASE_ALPHABETIC | Numeric formatting. Formats a numeric result as one or more occurrences of an lowercase alphabetic Latin character. |
| ARABIC | Numeric formatting. Formats a numeric result using Arabic cardinal numerals. |
| ARABIC_ABJAD | Numeric formatting. Formats a numeric result using ascending Abjad numerals. |
| ARABIC_ALPHA | Numeric formatting. Formats a numeric result using characters in the Arabic alphabet. |
| ARABIC_DASH | Numeric formatting. Formats a numeric result using Arabic cardinal numerals, with a prefix of "- " and a suffix of " -". |
| BAHT_TEXT | Numeric formatting. Formats a numeric result in the Thai counting system. |
| CARD_TEXT | Numeric formatting. Cardinal text (One, Two, Three, ...). |
| CHINESE_NUM1 | Numeric formatting. Formats a numeric result using ascending numbers from the appropriate counting system. |
| CHINESE_NUM2 | Numeric formatting. Formats a numeric result using sequential numbers from the appropriate legal format. |
| CHINESE_NUM3 | Numeric formatting. Formats a numeric result using sequential numbers from the appropriate counting thousand system. |
| CHOSUNG | Numeric formatting. Formats a numeric result using sequential numbers from the Korean Chosung format. |
| CIRCLE_NUM | Numeric formatting. Formats a numeric result using decimal numbering enclosed in a circle, using the enclosed alphanumeric glyph character for numbers in the range 1–20. |
| DB_CHAR | Numeric formatting. Formats a numeric result using double-byte Arabic numbering. |
| DB_NUM1 | Numeric formatting. Formats a numeric result using sequential digital ideographs, using the appropriate character. |
| DB_NUM2 | Numeric formatting. Formats a numeric result using sequential numbers from the appropriate counting system. |
| DB_NUM3 | Numeric formatting. Formats a numeric result using sequential numbers from the appropriate legal counting system. |
| DB_NUM4 | Numeric formatting. Formats a numeric result using sequential numbers from the appropriate digital counting system. |
| DOLLAR_TEXT | Numeric formatting. Dollar text (One, Two, Three, ... + AND 55/100). |
| GANADA | Numeric formatting. Formats a numeric result using sequential numbers from the Korean Ganada format. |
| GB1 | Numeric formatting. Formats a numeric result using decimal numbering followed by a period, using the enclosed alphanumeric glyph character. |
| GB2 | Numeric formatting. Formats a numeric result using decimal numbering enclosed in parenthesis, using the enclosed alphanumeric glyph character. |
| GB3 | Numeric formatting. Formats a numeric result using decimal numbering enclosed in a circle, using the enclosed alphanumeric glyph character. |
| GB4 | Numeric formatting. Formats a numeric result using decimal numbering enclosed in a circle, using the enclosed alphanumeric glyph character. |
| HEBREW1 | Numeric formatting. Formats a numeric result using Hebrew numerals. |
| HEBREW2 | Numeric formatting. Formats a numeric result using the Hebrew alphabet. |
| HEX | Numeric formatting. Formats the numeric result using uppercase hexadecimal digits. |
| HINDI_ARABIC | Numeric formatting. Formats a numeric result using Hindi numbers. |
| HINDI_CARD_TEXT | Numeric formatting. Formats a numeric result using sequential numbers from the Hindi counting system. |
| HINDI_LETTER1 | Numeric formatting. Formats a numeric result using Hindi vowels. |
| HINDI_LETTER2 | Numeric formatting. Formats a numeric result using Hindi consonants. |
| IROHA | Numeric formatting. Formats a numeric result using the Japanese iroha. |
| KANJI_NUM1 | Numeric formatting. Formats a numeric result using a Japanese style using the appropriate counting system. |
| KANJI_NUM2 | Numeric formatting. Formats a numeric result using the appropriate counting system. |
| KANJI_NUM3 | Numeric formatting. Formats a numeric result using the appropriate counting system. |
| ORDINAL | Numeric formatting. Ordinal (1st, 2nd, 3rd, ...). |
| ORD_TEXT | Numeric formatting. Ordinal text (First, Second, Third, ...). |
| UPPERCASE_ROMAN | Numeric formatting. Uppercase Roman (I, II, III, ...). |
| LOWERCASE_ROMAN | Numeric formatting. Lowercase Roman (i, ii, iii, ...). |
| SB_CHAR | Numeric formatting. Formats a numeric result using single-byte Arabic numbering. |
| THAI_ARABIC | Numeric formatting. Formats a numeric result using Thai numbers. |
| THAI_CARD_TEXT | Numeric formatting. Formats a numeric result using sequential numbers from the Thai counting system. |
| THAI_LETTER | Numeric formatting. Formats a numeric result using Thai letters. |
| VIET_CARD_TEXT | Numeric formatting. Formats a numeric result using Vietnamese numerals. |
| ZODIAC1 | Numeric formatting. Formats a numeric result using sequential numerical traditional ideographs. |
| ZODIAC2 | Numeric formatting. Formats a numeric result using sequential zodiac ideographs. |
| ZODIAC3 | Numeric formatting. Formats a numeric result using sequential traditional zodiac ideographs. |
| CAPS | Text formatting. Capitalizes the first letter of each word. |
| FIRST_CAP | Text formatting. Capitalizes the first letter of the first word. |
| LOWER | Text formatting. All letters are lowercase. |
| UPPER | Text formatting. All letters are uppercase. |
| CHAR_FORMAT | Field result formatting. The CHARFORMAT instruction. |
| MERGE_FORMAT | Field result formatting. The MERGEFORMAT instruction. |
| MERGE_FORMAT_INET | Field result formatting. The MERGEFORMATINET instruction. |

### Examples

Shows how to format field results.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Use a document builder to insert a field that displays a result with no format applied.
field = builder.insert_field("= 2 + 3")

self.assertEqual("= 2 + 3", field.get_field_code())
self.assertEqual("5", field.result)

# We can apply a format to a field's result using the field's properties.
# Below are three types of formats that we can apply to a field's result.
# 1 -  Numeric format:
format = field.format
format.numeric_format = "$###.00"
field.update()

self.assertEqual("= 2 + 3 \\# $###.00", field.get_field_code())
self.assertEqual("$  5.00", field.result)

# 2 -  Date/time format:
field = builder.insert_field("DATE")
format = field.format
format.date_time_format = "dddd, MMMM dd, yyyy"
field.update()

self.assertEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.get_field_code())
print(f"Today's date, in {format.date_time_format} format:\n\t{field.result}")

# 3 -  General format:
field = builder.insert_field("= 25 + 33")
format = field.format
format.general_formats.add(aw.fields.GeneralFormat.LOWERCASE_ROMAN)
format.general_formats.add(aw.fields.GeneralFormat.UPPER)
field.update()

for index, general_format in enumerate(format.general_formats):
    print(f"General format index {index}: {general_format}")

self.assertEqual("= 25 + 33 \\* roman \\* Upper", field.get_field_code())
self.assertEqual("LVIII", field.result)
self.assertEqual(2, format.general_formats.count)
self.assertEqual(aw.fields.GeneralFormat.LOWERCASE_ROMAN, format.general_formats[0])

# We can remove our formats to revert the field's result to its original form.
format.general_formats.remove(aw.fields.GeneralFormat.LOWERCASE_ROMAN)
format.general_formats.remove_at(0)
self.assertEqual(0, format.general_formats.count)
field.update()

self.assertEqual("= 25 + 33  ", field.get_field_code())
self.assertEqual("58", field.result)
self.assertEqual(0, format.general_formats.count)
```

### See Also

* module [aspose.words.fields](../)

