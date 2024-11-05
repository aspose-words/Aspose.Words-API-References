---
title: GeneralFormat Enum
linktitle: GeneralFormat
articleTitle: GeneralFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.GeneralFormat enum. Specifies a general format that is applied to a numeric text or any field result. A field may have a combination of general formats in C#.
type: docs
weight: 2990
url: /net/aspose.words.fields/generalformat/
---
## GeneralFormat enumeration

Specifies a general format that is applied to a numeric, text, or any field result. A field may have a combination of general formats.

```csharp
public enum GeneralFormat
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | Used to specify a missing general format. |
| Aiueo | `1` | Numeric formatting. Formats a numeric result using hiragana characters in the traditional a-i-u-e-o order. |
| UppercaseAlphabetic | `2` | Numeric formatting. Formats a numeric result as one or more occurrences of an uppercase alphabetic Latin character. |
| LowercaseAlphabetic | `3` | Numeric formatting. Formats a numeric result as one or more occurrences of an lowercase alphabetic Latin character. |
| Arabic | `4` | Numeric formatting. Formats a numeric result using Arabic cardinal numerals. |
| ArabicAbjad | `5` | Numeric formatting. Formats a numeric result using ascending Abjad numerals. |
| ArabicAlpha | `6` | Numeric formatting. Formats a numeric result using characters in the Arabic alphabet. |
| ArabicDash | `7` | Numeric formatting. Formats a numeric result using Arabic cardinal numerals, with a prefix of "- " and a suffix of " -". |
| BahtText | `8` | Numeric formatting. Formats a numeric result in the Thai counting system. |
| CardText | `9` | Numeric formatting. Cardinal text (One, Two, Three, ...). |
| ChineseNum1 | `10` | Numeric formatting. Formats a numeric result using ascending numbers from the appropriate counting system. |
| ChineseNum2 | `11` | Numeric formatting. Formats a numeric result using sequential numbers from the appropriate legal format. |
| ChineseNum3 | `12` | Numeric formatting. Formats a numeric result using sequential numbers from the appropriate counting thousand system. |
| Chosung | `13` | Numeric formatting. Formats a numeric result using sequential numbers from the Korean Chosung format. |
| CircleNum | `14` | Numeric formatting. Formats a numeric result using decimal numbering enclosed in a circle, using the enclosed alphanumeric glyph character for numbers in the range 1–20. |
| DBChar | `15` | Numeric formatting. Formats a numeric result using double-byte Arabic numbering. |
| DBNum1 | `16` | Numeric formatting. Formats a numeric result using sequential digital ideographs, using the appropriate character. |
| DBNum2 | `17` | Numeric formatting. Formats a numeric result using sequential numbers from the appropriate counting system. |
| DBNum3 | `18` | Numeric formatting. Formats a numeric result using sequential numbers from the appropriate legal counting system. |
| DBNum4 | `19` | Numeric formatting. Formats a numeric result using sequential numbers from the appropriate digital counting system. |
| DollarText | `20` | Numeric formatting. Dollar text (One, Two, Three, ... + AND 55/100). |
| Ganada | `21` | Numeric formatting. Formats a numeric result using sequential numbers from the Korean Ganada format. |
| GB1 | `22` | Numeric formatting. Formats a numeric result using decimal numbering followed by a period, using the enclosed alphanumeric glyph character. |
| GB2 | `23` | Numeric formatting. Formats a numeric result using decimal numbering enclosed in parenthesis, using the enclosed alphanumeric glyph character. |
| GB3 | `24` | Numeric formatting. Formats a numeric result using decimal numbering enclosed in a circle, using the enclosed alphanumeric glyph character. |
| GB4 | `25` | Numeric formatting. Formats a numeric result using decimal numbering enclosed in a circle, using the enclosed alphanumeric glyph character. |
| Hebrew1 | `26` | Numeric formatting. Formats a numeric result using Hebrew numerals. |
| Hebrew2 | `27` | Numeric formatting. Formats a numeric result using the Hebrew alphabet. |
| Hex | `28` | Numeric formatting. Formats the numeric result using uppercase hexadecimal digits. |
| HindiArabic | `29` | Numeric formatting. Formats a numeric result using Hindi numbers. |
| HindiCardText | `30` | Numeric formatting. Formats a numeric result using sequential numbers from the Hindi counting system. |
| HindiLetter1 | `31` | Numeric formatting. Formats a numeric result using Hindi vowels. |
| HindiLetter2 | `32` | Numeric formatting. Formats a numeric result using Hindi consonants. |
| Iroha | `33` | Numeric formatting. Formats a numeric result using the Japanese iroha. |
| KanjiNum1 | `34` | Numeric formatting. Formats a numeric result using a Japanese style using the appropriate counting system. |
| KanjiNum2 | `35` | Numeric formatting. Formats a numeric result using the appropriate counting system. |
| KanjiNum3 | `36` | Numeric formatting. Formats a numeric result using the appropriate counting system. |
| Ordinal | `37` | Numeric formatting. Ordinal (1st, 2nd, 3rd, ...). |
| OrdText | `38` | Numeric formatting. Ordinal text (First, Second, Third, ...). |
| UppercaseRoman | `39` | Numeric formatting. Uppercase Roman (I, II, III, ...). |
| LowercaseRoman | `40` | Numeric formatting. Lowercase Roman (i, ii, iii, ...). |
| SBChar | `41` | Numeric formatting. Formats a numeric result using single-byte Arabic numbering. |
| ThaiArabic | `42` | Numeric formatting. Formats a numeric result using Thai numbers. |
| ThaiCardText | `43` | Numeric formatting. Formats a numeric result using sequential numbers from the Thai counting system. |
| ThaiLetter | `44` | Numeric formatting. Formats a numeric result using Thai letters. |
| VietCardText | `45` | Numeric formatting. Formats a numeric result using Vietnamese numerals. |
| Zodiac1 | `46` | Numeric formatting. Formats a numeric result using sequential numerical traditional ideographs. |
| Zodiac2 | `47` | Numeric formatting. Formats a numeric result using sequential zodiac ideographs. |
| Zodiac3 | `48` | Numeric formatting. Formats a numeric result using sequential traditional zodiac ideographs. |
| Caps | `49` | Text formatting. Capitalizes the first letter of each word. |
| FirstCap | `50` | Text formatting. Capitalizes the first letter of the first word. |
| Lower | `51` | Text formatting. All letters are lowercase. |
| Upper | `52` | Text formatting. All letters are uppercase. |
| CharFormat | `53` | Field result formatting. The CHARFORMAT instruction. |
| MergeFormat | `54` | Field result formatting. The MERGEFORMAT instruction. |
| MergeFormatInet | `55` | Field result formatting. The MERGEFORMATINET instruction. |

## Examples

Shows how to format field results.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Use a document builder to insert a field that displays a result with no format applied.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// We can apply a format to a field's result using the field's properties.
// Below are three types of formats that we can apply to a field's result.
// 1 -  Numeric format:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 -  Date/time format:
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 -  General format:
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

// We can remove our formats to revert the field's result to its original form.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### See Also

* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
