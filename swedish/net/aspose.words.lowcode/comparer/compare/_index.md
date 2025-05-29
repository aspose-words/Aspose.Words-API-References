---
title: Comparer.Compare
linktitle: Compare
articleTitle: Compare
second_title: Aspose.Words för .NET
description: Jämför enkelt två dokument med vår jämförelsemetod. Spara skillnader och spåra redigeringar och formateringsändringar i en enda utdatafil.
type: docs
weight: 20
url: /sv/net/aspose.words.lowcode/comparer/compare/
---
## Compare(*string, string, string, string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_4}

Jämför två dokument med ytterligare alternativ och sparar skillnaderna i den angivna utdatafilen, producerar ändringar som ett antal redigerings- och formateringsrevisioner.

```csharp
public static void Compare(string v1, string v2, string outputFileName, string author, 
    DateTime dateTime, CompareOptions compareOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| v1 | String | Originaldokumentet. |
| v2 | String | Det modifierade dokumentet. |
| outputFileName | String | Namnet på utdatafilen. |
| author | String | Författarens initialer att använda för revideringar. |
| dateTime | DateTime | Datum och tid som ska användas för revisioner. |
| compareOptions | CompareOptions | Alternativ för dokumentjämförelse. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man enkelt jämför dokument.

```csharp
// Det finns flera sätt att jämföra dokument:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());

CompareOptions compareOptions = new CompareOptions();
compareOptions.IgnoreCaseChanges = true;
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), compareOptions);
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), compareOptions);
```

### Se även

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_2}

Jämför två dokument med ytterligare alternativ och sparar skillnaderna till den angivna utdatafilen i det angivna sparformatet, producerar ändringar som ett antal redigerings- och formatrevisioner.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| v1 | String | Originaldokumentet. |
| v2 | String | Det modifierade dokumentet. |
| outputFileName | String | Namnet på utdatafilen. |
| saveFormat | SaveFormat | Utdatas sparformat. |
| author | String | Författarens initialer att använda för revideringar. |
| dateTime | DateTime | Datum och tid som ska användas för revisioner. |
| compareOptions | CompareOptions | Alternativ för dokumentjämförelse. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man enkelt jämför dokument.

```csharp
// Det finns flera sätt att jämföra dokument:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());

CompareOptions compareOptions = new CompareOptions();
compareOptions.IgnoreCaseChanges = true;
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), compareOptions);
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), compareOptions);
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_3}

Jämför två dokument med ytterligare alternativ och sparar skillnaderna till den angivna utdatafilen i det angivna sparformatet, producerar ändringar som ett antal redigerings- och formatrevisioner.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveOptions saveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| v1 | String | Originaldokumentet. |
| v2 | String | Det modifierade dokumentet. |
| outputFileName | String | Namnet på utdatafilen. |
| saveOptions | SaveOptions | Utdatas sparalternativ. |
| author | String | Författarens initialer att använda för revideringar. |
| dateTime | DateTime | Datum och tid som ska användas för revisioner. |
| compareOptions | CompareOptions | Alternativ för dokumentjämförelse. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare}

Jämför två dokument som laddats från strömmar med ytterligare alternativ och sparar skillnaderna till den angivna utdataströmmen i det angivna sparformatet, producerar ändringar som ett antal redigerings- och formatrevisioner.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| v1 | Stream | Originaldokumentet. |
| v2 | Stream | Det modifierade dokumentet. |
| outputStream | Stream | Utgångsströmmen. |
| saveFormat | SaveFormat | Utdatas sparformat. |
| author | String | Författarens initialer att använda för revideringar. |
| dateTime | DateTime | Datum och tid som ska användas för revisioner. |
| compareOptions | CompareOptions | Alternativ för dokumentjämförelse. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata i den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda TIFF med flera bildrutor till den angivna strömmen.

## Exempel

Visar hur man jämför dokument från strömmen.

```csharp
// Det finns flera sätt att jämföra dokument från strömmen:
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime());

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
        {
            CompareOptions compareOptions = new CompareOptions();
            compareOptions.IgnoreCaseChanges = true;
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime(), compareOptions);
        }
    }
}
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_1}

Jämför två dokument som laddats från strömmar med ytterligare alternativ och sparar skillnaderna till den angivna utdataströmmen i det angivna sparformatet, producerar ändringar som ett antal redigerings- och formatrevisioner.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveOptions saveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| v1 | Stream | Originaldokumentet. |
| v2 | Stream | Det modifierade dokumentet. |
| outputStream | Stream | Utgångsströmmen. |
| saveOptions | SaveOptions | Utdatas sparalternativ. |
| author | String | Författarens initialer att använda för revideringar. |
| dateTime | DateTime | Datum och tid som ska användas för revisioner. |
| compareOptions | CompareOptions | Alternativ för dokumentjämförelse. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata i den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda TIFF med flera bildrutor till den angivna strömmen.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
