---
title: ShadowType Enum
linktitle: ShadowType
articleTitle: ShadowType
second_title: Aspose.Words för .NET
description: Aspose.Words.Drawing.ShadowType uppräkning. Anger typen av en formskugga i C#.
type: docs
weight: 1240
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
| ShadowMixed | `-2` | Ingen av fördefinierade skuggförinställningar. |
| Shadow1 | `1` | Första skuggtyp. |
| Shadow10 | `10` | Tionde skuggtyp. |
| Shadow11 | `11` | Elfte skuggtyp. |
| Shadow12 | `12` | Tolfte skuggtypen. |
| Shadow13 | `13` | Trettonde skuggtyp. |
| Shadow14 | `14` | Fjortonde skuggtyp. |
| Shadow15 | `15` | Femtonde skuggtyp. |
| Shadow16 | `16` | Sextonde skuggtyp. |
| Shadow17 | `17` | Sjuttonde skuggtyp. |
| Shadow18 | `18` | Artonde skuggtyp. |
| Shadow19 | `19` | Nittonde skuggtyp. |
| Shadow2 | `2` | Andra skuggtyp. |
| Shadow20 | `20` | Tjugonde skuggtyp. |
| Shadow21 | `21` | Tjugoförsta skuggtyp. |
| Shadow22 | `22` | Tjugo sekunders skuggtyp. |
| Shadow23 | `23` | Tjugotredje skuggtyp. |
| Shadow24 | `24` | Tjugofjärde skuggtyp. |
| Shadow25 | `25` | Tjugofemte skuggtyp. |
| Shadow26 | `26` | Tjugosjätte skuggtyp. |
| Shadow27 | `27` | Tjugosjunde skuggtyp. |
| Shadow28 | `28` | Tjugoåttonde skuggtyp. |
| Shadow29 | `29` | Tjugonionde skuggtyp. |
| Shadow3 | `3` | Tredje skuggtypen. |
| Shadow30 | `30` | Trettionde skuggtyp. |
| Shadow31 | `31` | Trettioförsta skuggtyp. |
| Shadow32 | `32` | Trettio sekunders skuggtyp. |
| Shadow33 | `33` | Trettiotredje skuggtyp. |
| Shadow34 | `34` | Trettiofjärde skuggtyp. |
| Shadow35 | `35` | Trettiofemte skuggtyp. |
| Shadow36 | `36` | Trettiosjätte skuggtyp. |
| Shadow37 | `37` | Trettiosjunde skuggtyp. |
| Shadow38 | `38` | Trettioåttonde skuggtyp. |
| Shadow39 | `39` | Trettionionde skuggtyp. |
| Shadow4 | `4` | Fjärde skuggtypen. |
| Shadow40 | `40` | Fyrtionde skuggtyp. |
| Shadow41 | `41` | Fyrtioförsta skuggtyp. |
| Shadow42 | `42` | Fyrtio sekunders skuggtyp. |
| Shadow43 | `43` | Fyrtiotredje skuggtyp. |
| Shadow5 | `5` | Femte skuggtyp. |
| Shadow6 | `6` | Sjätte skuggtypen. |
| Shadow7 | `7` | Sjunde skuggtypen. |
| Shadow8 | `8` | Åttonde skuggtyp. |
| Shadow9 | `9` | Nionde skuggtyp. |

## Anmärkningar

ShadowType är inte ett enkelt attribut, utan en förinställning som ställer in flera attribut samtidigt som bildar skuggans utseende.

## Exempel

Visar hur man arbetar med en skuggformatering för formen.

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
