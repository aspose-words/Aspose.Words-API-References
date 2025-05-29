---
title: Splitter.Split
linktitle: Split
articleTitle: Split
second_title: Aspose.Words för .NET
description: Dela enkelt upp dokument i flera avsnitt med vår flexibla Splitter Split-metod. Spara i ditt önskade format för enkel filhantering!
type: docs
weight: 40
url: /sv/net/aspose.words.lowcode/splitter/split/
---
## Split(*string, string, [SplitOptions](../../splitoptions/)*) {#split_2}

Delar upp ett dokument i flera delar baserat på de angivna delningsalternativen och sparar de resulterande delarna till filer. Utdatafilformatet bestäms av filändelsen på utdatafilnamnet.

```csharp
public static void Split(string inputFileName, string outputFileName, SplitOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen som används för att generera filnamn för dokumentdelar med regeln "outputFile_partIndex.extension" |
| options | SplitOptions | Alternativ för dokumentdelning. |

## Exempel

Visar hur man delar upp dokumentet efter sidor.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Se även

* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Split(*string, string, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split_3}

Delar upp ett dokument i flera delar baserat på de angivna delningsalternativen och sparar de resulterande delarna till filer i det angivna sparformatet.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    SplitOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen som används för att generera filnamn för dokumentdelar med regeln "outputFile_partIndex.extension" |
| saveFormat | SaveFormat | Sparformatet. |
| options | SplitOptions | Alternativ för dokumentdelning. |

## Exempel

Visar hur man delar upp dokumentet efter sidor.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Split(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_4}

Delar upp ett dokument i flera delar baserat på de angivna delningsalternativen och sparar de resulterande delarna till filer i det angivna sparformatet.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    SplitOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen som används för att generera filnamn för dokumentdelar med regeln "outputFile_partIndex.extension" |
| saveOptions | SaveOptions | Sparalternativen. |
| options | SplitOptions | Alternativ för dokumentdelning. |

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Split(*Stream, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split}

Delar upp ett dokument från en indataström i flera delar baserat på de angivna delningsalternativen och returnerar de resulterande delarna som en array av strömmar i det angivna sparformatet.

```csharp
public static Stream[] Split(Stream inputStream, SaveFormat saveFormat, SplitOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmen. |
| saveFormat | SaveFormat | Sparformatet. |
| options | SplitOptions | Alternativ för dokumentdelning. |

## Exempel

Visar hur man delar upp dokument från strömmen efter sidor.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitOptions options = new SplitOptions();
    options.SplitCriteria = SplitCriteria.Page;
    Stream[] stream = Splitter.Split(streamIn, SaveFormat.Docx, options);
}
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Split(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_1}

Delar upp ett dokument från en indataström i flera delar baserat på de angivna delningsalternativen och returnerar de resulterande delarna som en array av strömmar i det angivna sparformatet.

```csharp
public static Stream[] Split(Stream inputStream, SaveOptions saveOptions, SplitOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmen. |
| saveOptions | SaveOptions | Sparalternativen. |
| options | SplitOptions | Alternativ för dokumentdelning. |

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
