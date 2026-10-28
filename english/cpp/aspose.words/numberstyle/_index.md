---
title: Aspose::Words::NumberStyle enum
linktitle: NumberStyle
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NumberStyle enum. Specifies the number style for a list, footnotes and endnotes, page numbers in C++.'
type: docs
weight: 103750
url: /cpp/aspose.words/numberstyle/
---
## NumberStyle enum


Specifies the number style for a list, footnotes and endnotes, page numbers.

```cpp
enum class NumberStyle : int
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Aiueo | 20 | Aiueo full width |
| AiueoHalfWidth | 12 | Aiueo |
| Arabic | 0 | Arabic numbering (1, 2, 3, ...) |
| Arabic1 | 46 | Arabic alpha |
| Arabic2 | 48 | Arabic abjad |
| ArabicFullWidth | 14 | Full-width Arabic: 1, 2, 3, 4 |
| ArabicHalfWidth | 15 | Half-width Arabic: 1, 2, 3, 4 |
| Bullet | 23 | Bullet (check the character code in the text) |
| ChicagoManual | 9 | Chicago Manual of Style: *, †, † |
| Chosung | 25 | Korea Chosung |
| Custom | 65280 | Custom number format. It is supported by DOCX format only. |
| DecimalFullWidth | 19 | Decimal full width: 1, 2, 3, 4 |
| GB1 | 26 | Enclosed full stop |
| GB2 | 27 | Enclosed parenthesis |
| GB3 | 28 | Enclosed circle Chinese |
| GB4 | 29 | Ideograph enclosed circle |
| Ganada | 24 | Korean Ganada |
| Hangul | 43 | Korea legal |
| Hanja | 44 | Korea digital2 |
| HanjaRead | 41 | Korean digital |
| HanjaReadDigit | 42 | Korean counting |
| Hebrew1 | 45 | Hebrew-1 |
| Hebrew2 | 47 | Hebrew-2 |
| Hex | 8 | Hexadecimal: 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| HindiArabic | 51 | Hindi numbers |
| HindiCardinalText | 52 | Hindi descriptive (cardinals) |
| HindiLetter1 | 49 | Hindi vowels |
| HindiLetter2 | 50 | Hindi consonants |
| Iroha | 21 | Iroha full width |
| IrohaHalfWidth | 13 | Iroha |
| Kanji | 10 | Ideograph-digital |
| KanjiDigit | 11 | Japanese counting |
| KanjiTraditional | 16 | Japanese legal |
| KanjiTraditional2 | 17 | Japanese digital ten thousand |
| LeadingZero | 22 | Leading Zero (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| LowercaseLetter | 4 | Lower case letter (a, b, c, ...) |
| LowercaseRoman | 2 | Lower case Roman (i, ii, iii, ...) |
| LowercaseRussian | 58 | Lowercase Russian alphabet |
| None | 255 | No bullet or number. |
| Number | 6 | Numbered (One, Two, Three, ...) |
| NumberInCircle | 18 | Enclosed circles |
| NumberInDash | 57 | Page number format: - 1 -, - 2 -, - 3 -, - 4 - |
| Ordinal | 5 | Ordinal (1st, 2nd, 3rd, ...) |
| OrdinalText | 7 | Ordinal (text) (First, Second, Third, ...) |
| SimpChinNum1 | 37 | Chinese counting |
| SimpChinNum2 | 38 | Chinese legal simplified |
| SimpChinNum3 | 39 | Chinese counting thousand |
| SimpChinNum4 | 40 | Chinese (not implemented) |
| ThaiArabic | 54 | Thai numbers |
| ThaiCardinalText | 55 | Thai descriptive (cardinals) |
| ThaiLetter | 53 | Thai letters |
| TradChinNum1 | 33 | Taiwanese counting |
| TradChinNum2 | 34 | Ideograph legal traditional |
| TradChinNum3 | 35 | Taiwanese counting thousand |
| TradChinNum4 | 36 | Taiwanese digital |
| UppercaseLetter | 3 | Upper case Letter (A, B, C, ...) |
| UppercaseRoman | 1 | Upper case Roman (I, II, III, ...) |
| UppercaseRussian | 59 | Uppercase Russian alphabet |
| VietCardinalText | 56 | Vietnamese descriptive (cardinals) |
| Zodiac1 | 30 | Ideograph traditional |
| Zodiac2 | 31 | Ideograph Zodiac |
| Zodiac3 | 32 | Ideograph Zodiac traditional |

## Examples


Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level.
// We can begin and end a list by using a document builder's "ListFormat" property.
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Create a list from a Microsoft Word template, and customize the first two of its list levels.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(ListLevelAlignment::Right);
listLevel->set_NumberStyle(NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// This NumberFormat value will create star-shaped bullet list symbols.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Create paragraphs and apply both list levels of our custom list formatting to them.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
