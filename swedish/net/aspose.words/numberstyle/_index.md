---
title: NumberStyle Enum
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.NumberStyle-enum för att anpassa sidnummer i fotnoter och slutnoter, vilket enkelt förbättrar formateringen av ditt dokument.
type: docs
weight: 5040
url: /sv/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

Anger numreringsstilen för en lista, fotnoter och slutnoter, sidnummer.

```csharp
public enum NumberStyle
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Arabic | `0` | Arabisk numrering (1, 2, 3, ...) |
| UppercaseRoman | `1` | Romerska versaler (I, II, III, ...) |
| LowercaseRoman | `2` | Gemener romerska bokstäver (i, ii, iii, ...) |
| UppercaseLetter | `3` | Stor bokstav (A, B, C, ...) |
| LowercaseLetter | `4` | Gemener (a, b, c, ...) |
| Ordinal | `5` | Ordinal (1:a, 2:a, 3:a, ...) |
| Number | `6` | Numrerad (Ett, Två, Tre, ...) |
| OrdinalText | `7` | Ordinal (text) (Första, Andra, Tredje, ...) |
| Hex | `8` | Hexadecimalt: 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| ChicagoManual | `9` | Chicagos stilmanual: *, †, † |
| Kanji | `10` | Ideogram-digital |
| KanjiDigit | `11` | Japansk räkning |
| AiueoHalfWidth | `12` | Aiueo |
| IrohaHalfWidth | `13` | Iroha |
| ArabicFullWidth | `14` | Arabiska i full bredd: 1, 2, 3, 4 |
| ArabicHalfWidth | `15` | Halvbreddsarabiska: 1, 2, 3, 4 |
| KanjiTraditional | `16` | Japansk lag |
| KanjiTraditional2 | `17` | Japansk digital tiotusen |
| NumberInCircle | `18` | Inslutna cirklar |
| DecimalFullWidth | `19` | Decimal full bredd: 1, 2, 3, 4 |
| Aiueo | `20` | Aiueo full bredd |
| Iroha | `21` | Iroha full bredd |
| LeadingZero | `22` | Inledande nolla (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | `23` | Punkt (kontrollera teckenkoden i texten) |
| Ganada | `24` | Koreanska Ganada |
| Chosung | `25` | Korea Chosung |
| GB1 | `26` | Punkt innesluten |
| GB2 | `27` | Inkapslad parentes |
| GB3 | `28` | Sluten cirkel kinesisk |
| GB4 | `29` | Ideogram omsluten cirkel |
| Zodiac1 | `30` | Ideogram traditionellt |
| Zodiac2 | `31` | Ideogram Zodiac |
| Zodiac3 | `32` | Ideogram Zodiac traditionell |
| TradChinNum1 | `33` | Taiwanesisk räkning |
| TradChinNum2 | `34` | Ideogram juridisk traditionell |
| TradChinNum3 | `35` | Taiwanesisk räkning tusentals |
| TradChinNum4 | `36` | Taiwanesisk digital |
| SimpChinNum1 | `37` | Kinesisk räkning |
| SimpChinNum2 | `38` | Förenklad kinesisk rättsordning |
| SimpChinNum3 | `39` | Kinesisk räkning tusentals |
| SimpChinNum4 | `40` | Kinesiska (ej implementerad) |
| HanjaRead | `41` | Koreansk digital |
| HanjaReadDigit | `42` | Koreansk räkning |
| Hangul | `43` | Koreansk lag |
| Hanja | `44` | Korea digital2 |
| Hebrew1 | `45` | Hebreiska-1 |
| Arabic1 | `46` | Arabiska alfa |
| Hebrew2 | `47` | Hebreiska-2 |
| Arabic2 | `48` | arabiska abjad |
| HindiLetter1 | `49` | Hindi-vokaler |
| HindiLetter2 | `50` | Hindi-konsonanter |
| HindiArabic | `51` | Hindi-siffror |
| HindiCardinalText | `52` | Beskrivande på hindi (kardinaler) |
| ThaiLetter | `53` | Thailändska bokstäver |
| ThaiArabic | `54` | Thailändska siffror |
| ThaiCardinalText | `55` | Beskrivande thailändska (kardinaler) |
| VietCardinalText | `56` | Vietnamesiska beskrivande (kardinaler) |
| NumberInDash | `57` | Sidnummerformat: - 1 -, - 2 -, - 3 -, - 4 - |
| LowercaseRussian | `58` | Ryska alfabetet med gemener |
| UppercaseRussian | `59` | Ryska alfabetet med versaler |
| None | `255` | Ingen punkt eller siffra. |
| Custom | `65280` | Anpassat nummerformat. Stöds endast av DOCX-format. |

## Exempel

Visar hur man använder anpassad listformatering på stycken när man använder DocumentBuilder.

```csharp
Document doc = new Document();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
 // Vi kan skapa kapslade listor genom att öka indragsnivån.
 // Vi kan börja och avsluta en lista genom att använda dokumentbyggarens "ListFormat"-egenskap.
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
// Skapa en lista från en Microsoft Word-mall och anpassa de två första listnivåerna.
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
