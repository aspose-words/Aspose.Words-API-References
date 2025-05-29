---
title: ShadowType Enum
linktitle: ShadowType
articleTitle: ShadowType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.ShadowType-enum för att förbättra dina former med anpassningsbara skuggtyper för fantastiska dokumentbilder.
type: docs
weight: 1630
url: /sv/net/aspose.words.drawing/shadowtype/
---
## ShadowType enumeration

Anger typen av en formskugga.

```csharp
public enum ShadowType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| ShadowMixed | `-2` | Inga av de fördefinierade skuggförinställningarna. |
| Shadow1 | `1` | Första skuggtyp. |
| Shadow10 | `10` | Tionde skuggtyp. |
| Shadow11 | `11` | Elfte skuggtyp. |
| Shadow12 | `12` | Tolfte skuggtyp. |
| Shadow13 | `13` | Trettonde skuggtyp. |
| Shadow14 | `14` | Fjortonde skuggtyp. |
| Shadow15 | `15` | Femtonde skuggtyp. |
| Shadow16 | `16` | Sextonde skuggtyp. |
| Shadow17 | `17` | Sjuttonde skuggtyp. |
| Shadow18 | `18` | Artonde skuggtyp. |
| Shadow19 | `19` | Nittonde skuggtyp. |
| Shadow2 | `2` | Andra skuggtyp. |
| Shadow20 | `20` | Tjugonde skuggtyp. |
| Shadow21 | `21` | Typ av tjugoförsta skugga. |
| Shadow22 | `22` | Typ av skugga av typen tjugo sekunder. |
| Shadow23 | `23` | Typ av tjugotredje skugga. |
| Shadow24 | `24` | Tjugofyra skuggtyp. |
| Shadow25 | `25` | Tjugofemte skuggtyp. |
| Shadow26 | `26` | Typ av tjugosjätte skugga. |
| Shadow27 | `27` | Tjugosjunde skuggtyp. |
| Shadow28 | `28` | Typ av tjugoåttonde skugga. |
| Shadow29 | `29` | Tjugonionde skuggtyp. |
| Shadow3 | `3` | Tredje skuggtyp. |
| Shadow30 | `30` | Trettionde skuggtyp. |
| Shadow31 | `31` | Typ av trettioförsta skugga. |
| Shadow32 | `32` | Trettio sekunders skuggtyp. |
| Shadow33 | `33` | Trettiotre skuggtyp. |
| Shadow34 | `34` | Trettiofjärde skuggtyp. |
| Shadow35 | `35` | Trettiofemte skuggans typ. |
| Shadow36 | `36` | Typ av trettiosjätte skugga. |
| Shadow37 | `37` | Trettiosjunde skuggtyp. |
| Shadow38 | `38` | Trettioåttonde skuggtyp. |
| Shadow39 | `39` | Trettionionde skuggtyp. |
| Shadow4 | `4` | Fjärde skuggtyp. |
| Shadow40 | `40` | Fyrtionde skuggtyp. |
| Shadow41 | `41` | Fyrtioförsta skuggtypen. |
| Shadow42 | `42` | Fyrtio sekunders skuggtyp. |
| Shadow43 | `43` | Fyrtio tredje skuggtyp. |
| Shadow5 | `5` | Femte skuggatyp. |
| Shadow6 | `6` | Sjätte skuggtyp. |
| Shadow7 | `7` | Sjunde skuggtyp. |
| Shadow8 | `8` | Åttonde skuggatyp. |
| Shadow9 | `9` | Nionde skuggtyp. |

## Anmärkningar

Skuggtyp är inte ett enkelt attribut, utan en förinställning som samtidigt ställer in flera attribut som bildar skuggans utseende.

## Exempel

Visar hur man arbetar med skuggformatering för formen.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)
    shape.ShadowFormat.Clear();
```

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
