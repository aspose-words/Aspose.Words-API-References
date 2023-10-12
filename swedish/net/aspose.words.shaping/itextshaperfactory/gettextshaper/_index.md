---
title: ITextShaperFactory.GetTextShaper
second_title: Aspose.Words för .NET API Referens
description: ITextShaperFactory metod. Returnerar en ny instans av en textformare för teckensnittet som anges avfontPath ochfaceIndex .
type: docs
weight: 10
url: /sv/net/aspose.words.shaping/itextshaperfactory/gettextshaper/
---
## GetTextShaper(string, int) {#gettextshaper_1}

Returnerar en ny instans av en textformare för teckensnittet som anges av*fontPath* och*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontPath, int faceIndex)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fontPath | String | En absolut sökväg till teckensnittsfilen. |
| faceIndex | Int32 | Ett index över teckensnittet i TrueType-teckensnittssamlingen, eller 0 om angiven teckensnittsfil inte är TrueType-teckensnittssamling. |

### Se även

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* namnutrymme [Aspose.Words.Shaping](../../itextshaperfactory/)
* hopsättning [Aspose.Words](../../../)

---

## GetTextShaper(string, byte[], int) {#gettextshaper}

Returnerar ny instans av en textformare för teckensnittet som representeras av*fontBlob* och*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontId, byte[] fontBlob, int faceIndex)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fontId | String | En unik identifierare som unikt kan associeras med det angivna teckensnittet*fontBlob* . |
| fontBlob | Byte[] | Byte-array med teckensnittsdata. |
| faceIndex | Int32 | Ett index över teckensnittet i TrueType-teckensnittssamlingen, eller 0 om*fontBlob* är inte TrueType-teckensnittssamling. |

### Se även

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* namnutrymme [Aspose.Words.Shaping](../../itextshaperfactory/)
* hopsättning [Aspose.Words](../../../)


