---
title: ITextShaperFactory.GetTextShaper
linktitle: GetTextShaper
articleTitle: GetTextShaper
second_title: Aspose.Words för .NET
description: Upptäck ITextShaperFactorys GetTextShaper-metoden för att skapa en anpassad textformare för dina specifika teckensnittsbehov, vilket förbättrar din textrenderingsupplevelse.
type: docs
weight: 10
url: /sv/net/aspose.words.shaping/itextshaperfactory/gettextshaper/
---
## GetTextShaper(*string, int*) {#gettextshaper_1}

Returnerar en ny instans av en textformare för det teckensnitt som anges av*fontPath* och*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontPath, int faceIndex)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fontPath | String | En absolut sökväg till typsnittsfilen. |
| faceIndex | Int32 | Ett index över teckensnittet i TrueType-teckensnittssamlingen, eller 0 om den angivna teckensnittsfilen inte är en TrueType-teckensnittssamling. |

### Se även

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* namnutrymme [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* hopsättning [Aspose.Words](../../../)

---

## GetTextShaper(*string, byte[], int*) {#gettextshaper}

Returnerar en ny instans av en textformare för teckensnittet som representeras av*fontBlob* och*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontId, byte[] fontBlob, int faceIndex)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fontId | String | En unik identifierare som kan associeras unikt med det angivna teckensnittet*fontBlob* . |
| fontBlob | Byte[] | Byte-array med teckensnittsdata. |
| faceIndex | Int32 | Ett index över teckensnittet i TrueType-teckensnittssamlingen, eller 0 om*fontBlob* är inte en samling av TrueType-teckensnitt. |

### Se även

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* namnutrymme [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* hopsättning [Aspose.Words](../../../)
