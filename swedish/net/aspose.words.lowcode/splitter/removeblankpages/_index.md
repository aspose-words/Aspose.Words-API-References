---
title: Splitter.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words för .NET
description: Ta enkelt bort tomma sidor från dina dokument med metoden Splitter RemoveBlankPages. Spara tid och förbättra ditt arbetsflöde idag!
type: docs
weight: 30
url: /sv/net/aspose.words.lowcode/splitter/removeblankpages/
---
## RemoveBlankPages(*string, string*) {#removeblankpages_2}

Tar bort tomma sidor från dokumentet och sparar resultatet. Returnerar en lista över sidnummer som togs bort.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |

### Returvärde

Listan med sidnummer har betraktats som tom och tagits bort.

## Exempel

Visar hur man tar bort tomma sidor från dokumentet.

```csharp
// Det finns flera sätt att ta bort tomma sidor från dokumentet:
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### Se även

* class [Splitter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages_3}

Tar bort tomma sidor från dokumentet och sparar resultatet i det angivna formatet. Returnerar en lista över sidnummer som togs bort.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| saveFormat | SaveFormat | Sparformatet. |

### Returvärde

Listan med sidnummer har betraktats som tom och tagits bort.

## Exempel

Visar hur man tar bort tomma sidor från dokumentet.

```csharp
// Det finns flera sätt att ta bort tomma sidor från dokumentet:
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_4}

Tar bort tomma sidor från dokumentet och sparar resultatet i det angivna formatet. Returnerar en lista över sidnummer som togs bort.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| saveOptions | SaveOptions | Sparalternativen. |

### Returvärde

Listan med sidnummer har betraktats som tom och tagits bort.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages}

Tar bort tomma sidor från ett dokument som tillhandahålls i en indataström och sparar det uppdaterade dokumentet till en utdataström i det angivna sparformatet. Returnerar en lista över sidnummer som togs bort.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmen. |
| outputStream | Stream | Utgångsströmmen. |
| saveFormat | SaveFormat | Sparformatet. |

### Returvärde

Listan med sidnummer har betraktats som tom och tagits bort.

## Exempel

Visar hur man tar bort tomma sidor från dokumentet från strömmen.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Blank pages.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.RemoveBlankPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.RemoveBlankPages(streamIn, streamOut, SaveFormat.Docx);
}
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_1}

Tar bort tomma sidor från ett dokument som tillhandahålls i en indataström och sparar det uppdaterade dokumentet till en utdataström i det angivna sparformatet. Returnerar en lista över sidnummer som togs bort.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmen. |
| outputStream | Stream | Utgångsströmmen. |
| saveOptions | SaveOptions | Sparalternativen. |

### Returvärde

Listan med sidnummer har betraktats som tom och tagits bort.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
