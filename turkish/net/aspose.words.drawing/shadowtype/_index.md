---
title: ShadowType Enum
linktitle: ShadowType
articleTitle: ShadowType
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.ShadowType Sıralama. Şekil gölgesinin türünü belirtir C#'da.
type: docs
weight: 1240
url: /tr/net/aspose.words.drawing/shadowtype/
---
## ShadowType enumeration

Şekil gölgesinin türünü belirtir.

```csharp
public enum ShadowType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| ShadowMixed | `-2` | Önceden tanımlanmış gölge ön ayarlarından hiçbiri. |
| Shadow1 | `1` | İlk gölge türü. |
| Shadow10 | `10` | Onuncu gölge türü. |
| Shadow11 | `11` | Onbirinci gölge türü. |
| Shadow12 | `12` | Onikinci gölge türü. |
| Shadow13 | `13` | On üçüncü gölge türü. |
| Shadow14 | `14` | On dördüncü gölge türü. |
| Shadow15 | `15` | On beşinci gölge türü. |
| Shadow16 | `16` | On altıncı gölge türü. |
| Shadow17 | `17` | On yedinci gölge türü. |
| Shadow18 | `18` | On sekizinci gölge türü. |
| Shadow19 | `19` | On dokuzuncu gölge türü. |
| Shadow2 | `2` | İkinci gölge türü. |
| Shadow20 | `20` | Yirminci gölge türü. |
| Shadow21 | `21` | Yirmi birinci gölge türü. |
| Shadow22 | `22` | Yirmi ikinci gölge türü. |
| Shadow23 | `23` | Yirmi üçüncü gölge türü. |
| Shadow24 | `24` | Yirmi dördüncü gölge türü. |
| Shadow25 | `25` | Yirmi beşinci gölge türü. |
| Shadow26 | `26` | Yirmi altıncı gölge türü. |
| Shadow27 | `27` | Yirmi yedinci gölge türü. |
| Shadow28 | `28` | Yirmi sekizinci gölge türü. |
| Shadow29 | `29` | Yirmi dokuzuncu gölge türü. |
| Shadow3 | `3` | Üçüncü gölge türü. |
| Shadow30 | `30` | Otuzuncu gölge türü. |
| Shadow31 | `31` | Otuz birinci gölge türü. |
| Shadow32 | `32` | Otuz saniyelik gölge türü. |
| Shadow33 | `33` | Otuz üçüncü gölge türü. |
| Shadow34 | `34` | Otuz dördüncü gölge türü. |
| Shadow35 | `35` | Otuz beşinci gölge türü. |
| Shadow36 | `36` | Otuz altıncı gölge türü. |
| Shadow37 | `37` | Otuz yedinci gölge türü. |
| Shadow38 | `38` | Otuz sekizinci gölge türü. |
| Shadow39 | `39` | Otuz dokuzuncu gölge türü. |
| Shadow4 | `4` | Dördüncü gölge türü. |
| Shadow40 | `40` | Kırkıncı gölge türü. |
| Shadow41 | `41` | Kırk birinci gölge türü. |
| Shadow42 | `42` | Kırk ikinci gölge türü. |
| Shadow43 | `43` | Kırk üçüncü gölge türü. |
| Shadow5 | `5` | Beşinci gölge türü. |
| Shadow6 | `6` | Altıncı gölge türü. |
| Shadow7 | `7` | Yedinci gölge türü. |
| Shadow8 | `8` | Sekizinci gölge türü. |
| Shadow9 | `9` | Dokuzuncu gölge türü. |

## Notlar

ShadowType basit bir özellik değildir, ancak gölge görünümünü oluşturan birçok özelliği aynı anda ayarlayan bir ön ayardır.

## Örnekler

Şeklin gölge formatıyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)                
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)            
    shape.ShadowFormat.Clear();
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
