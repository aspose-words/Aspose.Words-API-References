---
title: PatternType Enum
linktitle: PatternType
articleTitle: PatternType
second_title: .NET için Aspose.Words
description: Şekillerinizi özelleştirilebilir dolgu desenleriyle geliştirmek için Aspose.Words.Drawing.PatternType enum'unu keşfedin. Belge tasarımınızı zahmetsizce yükseltin!
type: docs
weight: 1550
url: /tr/net/aspose.words.drawing/patterntype/
---
## PatternType enumeration

Bir şekli doldurmak için kullanılacak dolgu desenini belirtir.

```csharp
public enum PatternType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `-1` | Desen yok. |
| Percent10 | `1` | Ön plan renginin %10'u. |
| Percent20 | `2` | Ön plan renginin %20'si. |
| Percent25 | `3` | Ön plan renginin %25'i. |
| Percent30 | `4` | Ön plan renginin %30'u. |
| Percent40 | `5` | Ön plan renginin %40'ı |
| Percent50 | `6` | Ön plan renginin %50'si |
| Percent5 | `7` | Ön plan renginin %5'i. |
| Percent60 | `8` | Ön plan renginin %60'ı. |
| Percent70 | `9` | Ön plan renginin %70'i. |
| Percent75 | `10` | Ön plan renginin %75'i. |
| Percent80 | `11` | Ön plan renginin %80'i. |
| Percent90 | `12` | Ön plan renginin %90'ı. |
| Cross | `13` | Çapraz. |
| DarkDownwardDiagonal | `14` | Koyu aşağı doğru çapraz. |
| DarkHorizontal | `15` | Koyu yatay. |
| DarkUpwardDiagonal | `16` | Koyu yukarı çapraz. |
| DarkVertical | `17` | Koyu dikey. |
| DashedDownwardDiagonal | `18` | Aşağıya doğru çapraz çizgi. |
| DashedHorizontal | `19` | Yatay kesik çizgi. |
| DashedUpwardDiagonal | `20` | Yukarı doğru çapraz çizgiyle çizilmiştir. |
| DashedVertical | `21` | Dikey kesik çizgi. |
| DiagonalBrick | `22` | Çapraz tuğla. |
| DiagonalCross | `23` | Çapraz çapraz. |
| Divot | `24` | Desen çukuru. |
| DottedDiamond | `25` | Noktalı elmas. |
| DottedGrid | `26` | Noktalı ızgara. |
| DownwardDiagonal | `27` | Aşağıya doğru çapraz. |
| Horizontal | `28` | Yatay. |
| HorizontalBrick | `29` | Yatay tuğla. |
| LargeCheckerBoard | `30` | Büyük dama tahtası. |
| LargeConfetti | `31` | Büyük konfeti. |
| LargeGrid | `32` | Büyük ızgara. |
| LightDownwardDiagonal | `33` | Hafif aşağı doğru çapraz. |
| LightHorizontal | `34` | Hafif yatay. |
| LightUpwardDiagonal | `36` | Yukarı doğru çapraz ışık. |
| LightVertical | `37` | Hafif dikey. |
| NarrowHorizontal | `38` | Dar yatay. |
| NarrowVertical | `39` | Dar dikey. |
| OutlinedDiamond | `40` | Anahatları çizilmiş elmas. |
| Plaid | `41` | Ekose. |
| Shingle | `42` | Kiremit. |
| SmallCheckerBoard | `43` | Küçük dama tahtası. |
| SmallConfetti | `44` | Küçük konfeti. |
| SmallGrid | `45` | Küçük ızgara. |
| SolidDiamond | `46` | Masif elmas. |
| Sphere | `47` | Küre. |
| Trellis | `48` | Kafes. |
| UpwardDiagonal | `49` | Yukarı çapraz. |
| Vertical | `50` | Dikey. |
| Wave | `51` | Dalga. |
| Weave | `52` | Örgü. |
| WideDownwardDiagonal | `53` | Geniş aşağı doğru çapraz. |
| WideUpwardDiagonal | `54` | Geniş yukarı doğru çapraz. |
| ZigZag | `55` | Zikzak. |

## Örnekler

Bir şekle ait desenin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Bir deseni belirtilen dolguyla doldurmanın birkaç yolu vardır.
// 1 - Şekil dolgusuna desen uygula:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Şekil dolgusuna ön plan ve arka plan renkleriyle desen uygula:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
