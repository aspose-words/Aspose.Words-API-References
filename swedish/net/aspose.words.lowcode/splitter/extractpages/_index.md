---
title: Splitter.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words för .NET
description: Extrahera enkelt specifika sidor från valfritt dokument med vår Splitter ExtractPages-metod. Spara dem i önskat format för enkel åtkomst!
type: docs
weight: 20
url: /sv/net/aspose.words.lowcode/splitter/extractpages/
---
## ExtractPages(*string, string, int, int*) {#extractpages_4}

Extraherar ett angivet sidintervall från en dokumentfil och sparar de extraherade sidorna till en ny fil. Utdatafilformatet bestäms av filändelsen på utdatafilnamnet.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, int startPageIndex, 
    int pageCount)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| startPageIndex | Int32 | Det nollbaserade indexet för den första sidan som ska extraheras. |
| pageCount | Int32 | Antal sidor som ska extraheras. |

## Exempel

Visar hur man extraherar sidor från dokumentet.

```csharp
// Det finns flera sätt att extrahera sidor från dokumentet:
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### Se även

* class [Splitter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages_2}

Extraherar ett angivet sidintervall från en dokumentfil och sparar de extraherade sidorna till en ny fil med det angivna sparformatet.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| saveFormat | SaveFormat | Sparformatet. |
| startPageIndex | Int32 | Det nollbaserade indexet för den första sidan som ska extraheras. |
| pageCount | Int32 | Antal sidor som ska extraheras. |

## Exempel

Visar hur man extraherar sidor från dokumentet.

```csharp
// Det finns flera sätt att extrahera sidor från dokumentet:
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_3}

Extraherar ett angivet sidintervall från en dokumentfil och sparar de extraherade sidorna till en ny fil med det angivna sparformatet.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, int startPageIndex, int pageCount)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| saveOptions | SaveOptions | Sparalternativen. |
| startPageIndex | Int32 | Det nollbaserade indexet för den första sidan som ska extraheras. |
| pageCount | Int32 | Antal sidor som ska extraheras. |

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages}

Extraherar ett angivet sidintervall från en dokumentström och sparar de extraherade sidorna till en utdataström med det angivna sparformatet.

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmen. |
| outputStream | Stream | Utgångsströmmen. |
| saveFormat | SaveFormat | Sparformatet. |
| startPageIndex | Int32 | Det nollbaserade indexet för den första sidan som ska extraheras. |
| pageCount | Int32 | Antal sidor som ska extraheras. |

## Exempel

Visar hur man extraherar sidor från dokumentet från strömmen.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ExtractPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.ExtractPages(streamIn, streamOut, SaveFormat.Docx, 0, 2);
}
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_1}

Extraherar ett angivet sidintervall från en dokumentström och sparar de extraherade sidorna till en utdataström med det angivna sparformatet.

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    int startPageIndex, int pageCount)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmen. |
| outputStream | Stream | Utgångsströmmen. |
| saveOptions | SaveOptions | Sparalternativen. |
| startPageIndex | Int32 | Det nollbaserade indexet för den första sidan som ska extraheras. |
| pageCount | Int32 | Antal sidor som ska extraheras. |

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
