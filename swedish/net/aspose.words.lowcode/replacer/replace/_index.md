---
title: Replacer.Replace
linktitle: Replace
articleTitle: Replace
second_title: Aspose.Words för .NET
description: Ersätt enkelt alla förekomster av en specifik sträng i din indatafil med metoden Replacer. Effektivisera din textredigering idag!
type: docs
weight: 20
url: /sv/net/aspose.words.lowcode/replacer/replace/
---
## Replace(*string, string, string, string*) {#replace_8}

Ersätter alla förekomster av ett angivet teckensträngmönster med en ersättningssträng i indatafilen.

```csharp
public static int Replace(string inputFileName, string outputFileName, string pattern, 
    string replacement)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| pattern | String | En sträng som ska ersättas. |
| replacement | String | En sträng som ersätter alla förekomster av mönstret. |

### Returvärde

Antalet gjorda ersättningar.

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man ersätter strängar i dokumentet.

```csharp
// Det finns flera sätt att ersätta strängar i dokumentet:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.3.docx", SaveFormat.Docx, pattern, replacement, options);
```

### Se även

* class [Replacer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_4}

Ersätter alla förekomster av ett angivet teckensträngmönster med en ersättningssträng i indatafilen, med det angivna sparformatet och ytterligare alternativ.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| saveFormat | SaveFormat | Sparformatet. |
| pattern | String | En sträng som ska ersättas. |
| replacement | String | En sträng som ersätter alla förekomster av mönstret. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objekt för att ange ytterligare alternativ. |

### Returvärde

Antalet gjorda ersättningar.

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man ersätter strängar i dokumentet.

```csharp
// Det finns flera sätt att ersätta strängar i dokumentet:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.3.docx", SaveFormat.Docx, pattern, replacement, options);
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_6}

Ersätter alla förekomster av ett angivet teckensträngmönster med en ersättningssträng i indatafilen, med det angivna sparformatet och ytterligare alternativ.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| saveOptions | SaveOptions | Sparalternativen. |
| pattern | String | En sträng som ska ersättas. |
| replacement | String | En sträng som ersätter alla förekomster av mönstret. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objekt för att ange ytterligare alternativ. |

### Returvärde

Antalet gjorda ersättningar.

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace}

Ersätter alla förekomster av ett angivet teckensträngmönster med en ersättningssträng i indataströmmen, med det angivna sparformatet och ytterligare alternativ.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmen. |
| outputStream | Stream | Utgångsströmmen. |
| saveFormat | SaveFormat | Sparformatet. |
| pattern | String | En sträng som ska ersättas. |
| replacement | String | En sträng som ersätter alla förekomster av mönstret. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objekt för att ange ytterligare alternativ. |

### Returvärde

Antalet gjorda ersättningar.

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata i den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda TIFF med flera bildrutor till den angivna strömmen.

## Exempel

Visar hur man ersätter strängar i dokumentet med hjälp av dokument från strömmen.

```csharp
// Det finns flera sätt att ersätta strängar i dokumentet med hjälp av dokument från strömmen:
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
    {
        FindReplaceOptions options = new FindReplaceOptions();
        options.FindWholeWordsOnly = false;
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement, options);
    }
}
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_2}

Ersätter alla förekomster av ett angivet teckensträngmönster med en ersättningssträng i indataströmmen, med det angivna sparformatet och ytterligare alternativ.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmen. |
| outputStream | Stream | Utgångsströmmen. |
| saveOptions | SaveOptions | Sparalternativen. |
| pattern | String | En sträng som ska ersättas. |
| replacement | String | En sträng som ersätter alla förekomster av mönstret. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objekt för att ange ytterligare alternativ. |

### Returvärde

Antalet gjorda ersättningar.

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata i den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda TIFF med flera bildrutor till den angivna strömmen.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Replace(*string, string, Regex, string*) {#replace_9}

Ersätter alla förekomster av ett angivet teckensträngmönster med en ersättningssträng i indatafilen med hjälp av ett reguljärt uttryck.

```csharp
public static int Replace(string inputFileName, string outputFileName, Regex pattern, 
    string replacement)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| pattern | Regex | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| replacement | String | En sträng som ersätter alla förekomster av mönstret. |

### Returvärde

Antalet gjorda ersättningar.

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man ersätter strängar med regex i dokumentet.

```csharp
// Det finns flera sätt att ersätta strängar med regex i dokumentet:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.3.docx", SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### Se även

* class [Replacer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveFormat](../../../aspose.words/saveformat/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_5}

Ersätter alla förekomster av ett angivet teckensträngmönster med en ersättningssträng i indatafilen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| saveFormat | SaveFormat | Sparformatet. |
| pattern | Regex | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| replacement | String | En sträng som ersätter alla förekomster av mönstret. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objekt för att ange ytterligare alternativ. |

### Returvärde

Antalet gjorda ersättningar.

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man ersätter strängar med regex i dokumentet.

```csharp
// Det finns flera sätt att ersätta strängar med regex i dokumentet:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.3.docx", SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_7}

Ersätter alla förekomster av ett angivet teckensträngmönster med en ersättningssträng i indatafilen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ.

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| saveOptions | SaveOptions | Sparalternativen. |
| pattern | Regex | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| replacement | String | En sträng som ersätter alla förekomster av mönstret. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objekt för att ange ytterligare alternativ. |

### Returvärde

Antalet gjorda ersättningar.

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_1}

Ersätter alla förekomster av ett angivet teckensträngmönster med en ersättningssträng i indataströmmen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmen. |
| outputStream | Stream | Utgångsströmmen. |
| saveFormat | SaveFormat | Sparformatet. |
| pattern | Regex | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| replacement | String | En sträng som ersätter alla förekomster av mönstret. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objekt för att ange ytterligare alternativ. |

### Returvärde

Antalet gjorda ersättningar.

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata i den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda TIFF med flera bildrutor till den angivna strömmen.

## Exempel

Visar hur man ersätter strängar med regex i dokumentet med hjälp av dokument från strömmen.

```csharp
// Det finns flera sätt att ersätta strängar med regex i dokumentet med hjälp av dokument från strömmen:
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStreamRegex.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStreamRegex.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
}
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_3}

Ersätter alla förekomster av ett angivet teckensträngmönster med en ersättningssträng i indataströmmen med hjälp av ett reguljärt uttryck, med det angivna sparformatet och ytterligare alternativ.

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmen. |
| outputStream | Stream | Utgångsströmmen. |
| saveOptions | SaveOptions | Sparalternativen. |
| pattern | Regex | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| replacement | String | En sträng som ersätter alla förekomster av mönstret. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objekt för att ange ytterligare alternativ. |

### Returvärde

Antalet gjorda ersättningar.

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata i den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda TIFF med flera bildrutor till den angivna strömmen.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
