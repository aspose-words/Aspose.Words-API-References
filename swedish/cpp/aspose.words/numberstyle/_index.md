---
title: "Aspose::Words::NumberStyle enum"
linktitle: "NumberStyle"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::NumberStyle-enum. Anger numreringsstilen för en lista, fotnoter och slutnoter, sidnummer i C++."
type: docs
weight: 103000
url: /sv/cpp/aspose.words/numberstyle/
---
## NumberStyle enum


Anger siffrastilen för en lista, fotnoter och slutnoter samt sidnummer.

```cpp
enum class NumberStyle
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Arabiska | 0 | Arabisk numrering (1, 2, 3, ...) |
| UppercaseRoman | 1 | Stora romerska (I, II, III, ...) |
| LowercaseRoman | 2 | Små romerska (i, ii, iii, ...) |
| UppercaseLetter | 3 | Stora bokstäver (A, B, C, ...) |
| LowercaseLetter | 4 | Små bokstäver (a, b, c, ...) |
| Ordinal | 5 | Ordinal (1:a, 2:a, 3:e, ...) |
| Number | 6 | Numrerad (Ett, Två, Tre, ...) |
| OrdinalText | 7 | Ordinal (text) (Första, Andra, Tredje, ...) |
| Hex | 8 | Hexadecimal: 8, 9, A, B, C, D, E, F, 10, 11, 12. |
| ChicagoManual | 9 | Chicago Manual för [Style](../style/): *, †, † |
| Kanji | 10 | Ideograf-digital. |
| KanjiDigit | 11 | Japansk räkning. |
| AiueoHalfWidth | 12 | Aiueo. |
| IrohaHalfWidth | 13 | Iroha. |
| ArabicFullWidth | 14 | Fullbredd Arabiska: 1, 2, 3, 4. |
| ArabicHalfWidth | 15 | Halvbredd Arabiska: 1, 2, 3, 4. |
| KanjiTraditional | 16 | Japansk juridisk. |
| KanjiTraditional2 | 17 | Japansk digital tiotusen. |
| NumberInCircle | 18 | Inneslutna cirklar. |
| DecimalFullWidth | 19 | Decimal full bredd: 1, 2, 3, 4. |
| Aiueo | 20 | Aiueo full bredd. |
| Iroha | 21 | Iroha full bredd. |
| LeadingZero | 22 | Inledande noll (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Punkt | 23 | Punkt (kontrollera teckenkoden i texten) |
| Ganada | 24 | Koreanska Ganada. |
| Chosung | 25 | Korea Chosung. |
| GB1 | 26 | Innesluten punkt. |
| GB2 | 27 | Innesluten parentes. |
| GB3 | 28 | Innesluten kinesisk cirkel. |
| GB4 | 29 | Ideograf innesluten cirkel. |
| Zodiac1 | 30 | Ideograf traditionell. |
| Zodiac2 | 31 | Ideograf Zodiak. |
| Zodiac3 | 32 | Ideograf Zodiak traditionell. |
| TradChinNum1 | 33 | Taiwanesisk räkning. |
| TradChinNum2 | 34 | Ideograf juridisk traditionell. |
| TradChinNum3 | 35 | Taiwanesisk räkning tusen. |
| TradChinNum4 | 36 | Taiwanesisk digital. |
| SimpChinNum1 | 37 | Kinesisk räkning. |
| SimpChinNum2 | 38 | Kinesisk juridisk förenklad. |
| SimpChinNum3 | 39 | Kinesisk räkning tusen. |
| SimpChinNum4 | 40 | Kinesisk (inte implementerad) |
| HanjaRead | 41 | Koreansk digital. |
| HanjaReadDigit | 42 | Koreansk räkning. |
| Hangul | 43 | Koreansk juridisk. |
| Hanja | 44 | Koreansk digital2. |
| Hebrew1 | 45 | Hebrew-1. |
| Arabic1 | 46 | Arabisk alfa. |
| Hebrew2 | 47 | Hebrew-2. |
| Arabic2 | 48 | Arabisk abjad. |
| HindiLetter1 | 49 | Hindi vokaler. |
| HindiLetter2 | 50 | Hindi konsonanter. |
| HindiArabic | 51 | Hindi nummer. |
| HindiCardinalText | 52 | Hindi beskrivande (kardinaler) |
| ThaiLetter | 53 | Thai bokstäver. |
| ThaiArabic | 54 | Thai nummer. |
| ThaiCardinalText | 55 | Thai beskrivande (kardinaler) |
| VietCardinalText | 56 | Vietnamese beskrivande (kardinaler) |
| NumberInDash | 57 | Sidnummerformat: - 1 -, - 2 -, - 3 -, - 4 -. |
| Liten rysk | 58 | Liten rysk alfabet. |
| Stor rysk | 59 | Stor rysk alfabet. |
| None | 255 | Ingen punktlista eller nummer. |
| Anpassad | 65280 | Anpassat talformat. Det stöds endast av DOCX-format. |


## Exempel



Visar hur man tillämpar anpassad listformatering på stycken när man använder [DocumentBuilder](../documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
// Vi kan skapa nästlade listor genom att öka indragnivån.
// Vi kan börja och avsluta en lista genom att använda en dokumentbyggares egenskap "ListFormat".
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
// Skapa en lista från en Microsoft Word‑mall och anpassa de två första nivåerna i dess lista.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// Detta NumberFormat‑värde kommer att skapa stjärnformade punktlistsymboler.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Skapa stycken och tillämpa båda listnivåerna i vår anpassade listformatering på dem.
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

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
