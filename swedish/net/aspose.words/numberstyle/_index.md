---
title: NumberStyle
second_title: Aspose.Words för .NET API Referens
description: Anger nummerstilen för en lista fotnoter och slutnoter sidnummer.
type: docs
weight: 4070
url: /sv/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

Anger nummerstilen för en lista, fotnoter och slutnoter, sidnummer.

```csharp
public enum NumberStyle
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Arabic | `0` | Arabisk numrering (1, 2, 3, ...) |
| UppercaseRoman | `1` | Versaler Roman (I, II, III, ...) |
| LowercaseRoman | `2` | Gemener Roman (i, ii, iii, ...) |
| UppercaseLetter | `3` | Versaler (A, B, C, ...) |
| LowercaseLetter | `4` | Gemener (a, b, c, ...) |
| Ordinal | `5` | Ordinal (1:a, 2:a, 3:a, ...) |
| Number | `6` | Numrerad (ett, två, tre, ...) |
| OrdinalText | `7` | Ordinal (text) (Första, Andra, Tredje, ...) |
| Hex | `8` | Hexadecimal: 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| ChicagoManual | `9` | Chicago Manual of Style: *, †, † |
| Kanji | `10` | Ideograph-digital |
| KanjiDigit | `11` | Japansk räkning |
| AiueoHalfWidth | `12` | Aiueo |
| IrohaHalfWidth | `13` | Iroha |
| ArabicFullWidth | `14` | Fullbreddsarabiska: 1, 2, 3, 4 |
| ArabicHalfWidth | `15` | Halvbredd arabiska: 1, 2, 3, 4 |
| KanjiTraditional | `16` | Japanska legal |
| KanjiTraditional2 | `17` | Japansk digital tiotusen |
| NumberInCircle | `18` | Slutna cirklar |
| DecimalFullWidth | `19` | Decimal full bredd: 1, 2, 3, 4 |
| Aiueo | `20` | Aiueo full width |
| Iroha | `21` | Iroha full width |
| LeadingZero | `22` | Ledande noll (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | `23` | Bullet (kolla teckenkoden i texten) |
| Ganada | `24` | Koreanska Ganada |
| Chosung | `25` | Korea Chosung |
| GB1 | `26` | Bifogat punkt |
| GB2 | `27` | Bifogad parentes |
| GB3 | `28` | Omsluten cirkel Chinese |
| GB4 | `29` | Ideograf omsluten cirkel |
| Zodiac1 | `30` | Ideograph traditional |
| Zodiac2 | `31` | Ideograph Zodiac |
| Zodiac3 | `32` | Ideograph Zodiac traditionell |
| TradChinNum1 | `33` | taiwanesisk räkning |
| TradChinNum2 | `34` | Ideograph legal traditional |
| TradChinNum3 | `35` | Taiwanesiska räknar tusen |
| TradChinNum4 | `36` | Taiwanesiska digitala |
| SimpChinNum1 | `37` | Kinesisk räkning |
| SimpChinNum2 | `38` | Kinesisk juridisk förenklad |
| SimpChinNum3 | `39` | kinesiska räknar tusen |
| SimpChinNum4 | `40` | kinesiska (ej implementerad) |
| HanjaRead | `41` | Koreansk digital |
| HanjaReadDigit | `42` | Koreansk räkning |
| Hangul | `43` | Korea legal |
| Hanja | `44` | Korea digital2 |
| Hebrew1 | `45` | hebreiska-1 |
| Arabic1 | `46` | Arabiska alpha |
| Hebrew2 | `47` | Hebrew-2 |
| Arabic2 | `48` | Arabiska abjad |
| HindiLetter1 | `49` | hindivokaler |
| HindiLetter2 | `50` | Hindi-konsonanter |
| HindiArabic | `51` | Hindi siffror |
| HindiCardinalText | `52` | Hindi beskrivande (kardinaler) |
| ThaiLetter | `53` | thailändska bokstäver |
| ThaiArabic | `54` | thailändska siffror |
| ThaiCardinalText | `55` | Thai beskrivande (kardinaler) |
| VietCardinalText | `56` | vietnamesiska beskrivande (kardinaler) |
| NumberInDash | `57` | Sidnummerformat: - 1 -, - 2 -, - 3 -, - 4 - |
| LowercaseRussian | `58` | Ryska alfabetet med små bokstäver |
| UppercaseRussian | `59` | Ryska alfabetet med versaler |
| None | `255` | Ingen kula eller nummer. |
| Custom | `65280` | Anpassat nummerformat. Det stöds endast av DOCX-format. |

### Exempel

Visar hur du använder anpassad listformatering på stycken när du använder DocumentBuilder.

```csharp
Document doc = new Document();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
// Vi kan skapa kapslade listor genom att öka indragsnivån. 
// Vi kan börja och avsluta en lista genom att använda en dokumentbyggares "ListFormat"-egenskap. 
// Varje stycke som vi lägger till mellan en listas början och slutet kommer att bli ett objekt i listan.
// Skapa en lista från en Microsoft Word-mall och anpassa de två första av listnivåerna.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// Detta NumberFormat-värde skapar stjärnformade punktlistsymboler.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Skapa stycken och tillämpa båda listnivåerna i vår anpassade listformatering på dem.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
