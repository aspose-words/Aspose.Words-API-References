---
title: NumberStyle Enum
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.NumberStyle per personalizzare i numeri di pagina delle note a piè di pagina e delle note di chiusura, migliorando senza sforzo la formattazione del tuo documento.
type: docs
weight: 5040
url: /it/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

Specifica lo stile numerico per un elenco, note a piè di pagina e note di chiusura, numeri di pagina.

```csharp
public enum NumberStyle
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Arabic | `0` | Numerazione araba (1, 2, 3, ...) |
| UppercaseRoman | `1` | Romano maiuscolo (I, II, III, ...) |
| LowercaseRoman | `2` | Romano minuscolo (i, ii, iii, ...) |
| UppercaseLetter | `3` | Lettera maiuscola (A, B, C, ...) |
| LowercaseLetter | `4` | Lettera minuscola (a, b, c, ...) |
| Ordinal | `5` | Ordinale (1°, 2°, 3°, ...) |
| Number | `6` | Numerato (Uno, Due, Tre, ...) |
| OrdinalText | `7` | Ordinale (testo) (Primo, Secondo, Terzo, ...) |
| Hex | `8` | Esadecimale: 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| ChicagoManual | `9` | Manuale di stile di Chicago: *, †, † |
| Kanji | `10` | Ideogramma-digitale |
| KanjiDigit | `11` | Conteggio giapponese |
| AiueoHalfWidth | `12` | Aiueo |
| IrohaHalfWidth | `13` | Iroha |
| ArabicFullWidth | `14` | Arabo a larghezza intera: 1, 2, 3, 4 |
| ArabicHalfWidth | `15` | Arabo a mezza larghezza: 1, 2, 3, 4 |
| KanjiTraditional | `16` | Legale giapponese |
| KanjiTraditional2 | `17` | Diecimila digitali giapponesi |
| NumberInCircle | `18` | Cerchi chiusi |
| DecimalFullWidth | `19` | Larghezza decimale intera: 1, 2, 3, 4 |
| Aiueo | `20` | Aiueo a tutta larghezza |
| Iroha | `21` | Iroha a tutta larghezza |
| LeadingZero | `22` | Zero iniziale (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | `23` | Punto elenco (controlla il codice del carattere nel testo) |
| Ganada | `24` | Ganada coreano |
| Chosung | `25` | Corea Chosung |
| GB1 | `26` | Punto chiuso |
| GB2 | `27` | Parentesi racchiusa |
| GB3 | `28` | Cerchio chiuso cinese |
| GB4 | `29` | Ideogramma cerchio racchiuso |
| Zodiac1 | `30` | Ideogramma tradizionale |
| Zodiac2 | `31` | Ideogramma Zodiaco |
| Zodiac3 | `32` | Ideogramma Zodiaco tradizionale |
| TradChinNum1 | `33` | Conteggio taiwanese |
| TradChinNum2 | `34` | Ideogramma legale tradizionale |
| TradChinNum3 | `35` | Taiwanese che conta migliaia |
| TradChinNum4 | `36` | digitale taiwanese |
| SimpChinNum1 | `37` | Conteggio cinese |
| SimpChinNum2 | `38` | Cinese legale semplificato |
| SimpChinNum3 | `39` | conteggio cinese mille |
| SimpChinNum4 | `40` | Cinese (non implementato) |
| HanjaRead | `41` | digitale coreano |
| HanjaReadDigit | `42` | conteggio coreano |
| Hangul | `43` | Legalità in Corea |
| Hanja | `44` | Corea digitale2 |
| Hebrew1 | `45` | Ebraico-1 |
| Arabic1 | `46` | Arabo alfa |
| Hebrew2 | `47` | Ebraico-2 |
| Arabic2 | `48` | Arabo abjad |
| HindiLetter1 | `49` | Vocali hindi |
| HindiLetter2 | `50` | Consonanti hindi |
| HindiArabic | `51` | Numeri hindi |
| HindiCardinalText | `52` | Descrittivo hindi (cardinali) |
| ThaiLetter | `53` | Lettere tailandesi |
| ThaiArabic | `54` | Numeri tailandesi |
| ThaiCardinalText | `55` | Descrittivo tailandese (cardinali) |
| VietCardinalText | `56` | Descrittivo vietnamita (cardinali) |
| NumberInDash | `57` | Formato del numero di pagina: - 1 -, - 2 -, - 3 -, - 4 - |
| LowercaseRussian | `58` | Alfabeto russo minuscolo |
| UppercaseRussian | `59` | Alfabeto russo maiuscolo |
| None | `255` | Nessun punto elenco o numero. |
| Custom | `65280` | Formato numerico personalizzato. È supportato solo dal formato DOCX. |

## Esempi

Mostra come applicare la formattazione personalizzata degli elenchi ai paragrafi quando si utilizza DocumentBuilder.

```csharp
Document doc = new Document();

// Un elenco ci consente di organizzare e decorare serie di paragrafi con simboli di prefisso e rientri.
 // Possiamo creare elenchi annidati aumentando il livello di rientro.
 // Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" di un generatore di documenti.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
// Crea un elenco da un modello di Microsoft Word e personalizza i primi due livelli dell'elenco.
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

// Questo valore NumberFormat creerà simboli di elenchi puntati a forma di stella.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Crea paragrafi e applica loro entrambi i livelli di elenco della nostra formattazione di elenco personalizzata.
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

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
