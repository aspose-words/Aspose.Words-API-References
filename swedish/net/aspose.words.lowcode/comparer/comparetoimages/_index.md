---
title: Comparer.CompareToImages
linktitle: CompareToImages
articleTitle: CompareToImages
second_title: Aspose.Words för .NET
description: Jämför dokument enkelt med CompareToImages, spara skillnader som bilder för varje sida, vilket förbättrar tydlighet och visuell analys.
type: docs
weight: 30
url: /sv/net/aspose.words.lowcode/comparer/comparetoimages/
---
## CompareToImages(*string, string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages_1}

Jämför två dokument och sparar skillnaderna som bilder. Varje objekt i den returnerade arrayen representerar en enda sida av utdata som återges som en bild.

```csharp
public static Stream[] CompareToImages(string v1, string v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| v1 | String | Originaldokumentet. |
| v2 | String | Det modifierade dokumentet. |
| imageSaveOptions | ImageSaveOptions | Alternativ för att spara bilden i utdata. |
| author | String | Författarens initialer att använda för revideringar. |
| dateTime | DateTime | Datum och tid som ska användas för revisioner. |
| compareOptions | CompareOptions | Alternativ för dokumentjämförelse. |

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## CompareToImages(*Stream, Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages}

Jämför två dokument och sparar skillnaderna som bilder. Varje objekt i den returnerade arrayen representerar en enda sida av utdata som återges som en bild.

```csharp
public static Stream[] CompareToImages(Stream v1, Stream v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| v1 | Stream | Originaldokumentet. |
| v2 | Stream | Det modifierade dokumentet. |
| imageSaveOptions | ImageSaveOptions | Alternativ för att spara bilden i utdata. |
| author | String | Författarens initialer att använda för revideringar. |
| dateTime | DateTime | Datum och tid som ska användas för revisioner. |
| compareOptions | CompareOptions | Alternativ för dokumentjämförelse. |

## Exempel

Visar hur man jämför dokument och sparar resultat som bilder.

```csharp
// Det finns flera sätt att jämföra dokument:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Stream[] pages = Comparer.CompareToImages(firstDoc, secondDoc, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime());

using (FileStream firstStreamIn = new FileStream(firstDoc, FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(secondDoc, FileMode.Open, FileAccess.Read))
    {
        CompareOptions compareOptions = new CompareOptions();
        compareOptions.IgnoreCaseChanges = true;
        pages = Comparer.CompareToImages(firstStreamIn, secondStreamIn, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime(), compareOptions);
    }
}
```

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
