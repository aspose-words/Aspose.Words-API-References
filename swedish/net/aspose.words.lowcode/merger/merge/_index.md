---
title: Merger.Merge
second_title: Aspose.Words för .NET API Referens
description: Merger metod. Slår samman de givna indatadokumenten till ett enda utdatadokument med angivna in och utdatafilnamn.
type: docs
weight: 10
url: /sv/net/aspose.words.lowcode/merger/merge/
---
## Merge(string, string[]) {#merge_4}

Slår samman de givna indatadokumenten till ett enda utdatadokument med angivna in- och utdatafilnamn.

```csharp
public static void Merge(string outputFile, string[] inputFiles)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| outputFile | String | Utdatafilens namn. |
| inputFiles | String[] | Indatafilens namn. |

### Anmärkningar

Som standardKeepSourceFormatting är använd.

### Exempel

Visar hur man slår samman dokument till ett enda utdatadokument.

```csharp
//Det finns flera sätt att slå samman dokument:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Se även

* class [Merger](../)
* namnutrymme [Aspose.Words.LowCode](../../merger/)
* hopsättning [Aspose.Words](../../../)

---

## Merge(string, string[], SaveFormat, MergeFormatMode) {#merge_5}

Slår samman de givna indatadokumenten till ett enda utdatadokument med hjälp av specificerade indatautdatafilnamn och det slutliga dokumentformatet.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveFormat saveFormat, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| outputFile | String | Utdatafilens namn. |
| inputFiles | String[] | Indatafilens namn. |
| saveFormat | SaveFormat | Spara formatet. |
| mergeFormatMode | MergeFormatMode | Anger hur man slår samman formatering som krockar. |

### Exempel

Visar hur man slår samman dokument till ett enda utdatadokument.

```csharp
//Det finns flera sätt att slå samman dokument:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namnutrymme [Aspose.Words.LowCode](../../merger/)
* hopsättning [Aspose.Words](../../../)

---

## Merge(string, string[], SaveOptions, MergeFormatMode) {#merge_6}

Slår samman de givna indatadokumenten till ett enda utdatadokument med hjälp av specificerade utdatafilnamn och sparaalternativ.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| outputFile | String | Utdatafilens namn. |
| inputFiles | String[] | Indatafilens namn. |
| saveOptions | SaveOptions | Spara alternativen. |
| mergeFormatMode | MergeFormatMode | Anger hur man slår samman formatering som krockar. |

### Exempel

Visar hur man slår samman dokument till ett enda utdatadokument.

```csharp
//Det finns flera sätt att slå samman dokument:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namnutrymme [Aspose.Words.LowCode](../../merger/)
* hopsättning [Aspose.Words](../../../)

---

## Merge(string[], MergeFormatMode) {#merge_1}

Slår samman de givna indatadokumenten till ett enda dokument och returnerar[`Document`](../../../aspose.words/document/) instans av det slutliga dokumentet.

```csharp
public static Document Merge(string[] inputFiles, MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFiles | String[] | Indatafilens namn. |
| mergeFormatMode | MergeFormatMode | Anger hur man slår samman formatering som krockar. |

### Exempel

Visar hur man slår samman dokument till ett enda utdatadokument.

```csharp
//Det finns flera sätt att slå samman dokument:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Se även

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namnutrymme [Aspose.Words.LowCode](../../merger/)
* hopsättning [Aspose.Words](../../../)

---

## Merge(Stream, Stream[], SaveFormat) {#merge_2}

Slår samman de givna indatadokumenten till ett enda utdatadokument med hjälp av specificerade utdataströmmar och det slutliga dokumentformatet.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| outputStream | Stream | Utgångsströmmen. |
| inputStreams | Stream[] | Ingångsströmmarna. |
| saveFormat | SaveFormat | Spara formatet. |

### Exempel

Visar hur man slår samman dokument från stream till ett enda utdatadokument.

```csharp
//Det finns flera sätt att slå samman dokument från stream:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveOptions.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveFormat.docx", FileMode.Create, FileAccess.ReadWrite))                    
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        Document doc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        doc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.DocumentInstance.docx");
    }
}
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Merger](../)
* namnutrymme [Aspose.Words.LowCode](../../merger/)
* hopsättning [Aspose.Words](../../../)

---

## Merge(Stream, Stream[], SaveOptions, MergeFormatMode) {#merge_3}

Slår samman de givna indatadokumenten till ett enda utdatadokument med hjälp av specificerade utdataströmmar och sparaalternativ.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| outputStream | Stream | Utgångsströmmen. |
| inputStreams | Stream[] | Ingångsströmmarna. |
| saveOptions | SaveOptions | Spara alternativen. |
| mergeFormatMode | MergeFormatMode | Anger hur man slår samman formatering som krockar. |

### Exempel

Visar hur man slår samman dokument från stream till ett enda utdatadokument.

```csharp
//Det finns flera sätt att slå samman dokument från stream:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveOptions.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveFormat.docx", FileMode.Create, FileAccess.ReadWrite))                    
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        Document doc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        doc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.DocumentInstance.docx");
    }
}
```

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namnutrymme [Aspose.Words.LowCode](../../merger/)
* hopsättning [Aspose.Words](../../../)

---

## Merge(Stream[], MergeFormatMode) {#merge}

Slår samman de givna indatadokumenten till ett enda dokument och returnerar[`Document`](../../../aspose.words/document/) instans av det slutliga dokumentet.

```csharp
public static Document Merge(Stream[] inputStreams, MergeFormatMode mergeFormatMode)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStreams | Stream[] | Ingångsströmmarna. |
| mergeFormatMode | MergeFormatMode | Anger hur man slår samman formatering som krockar. |

### Exempel

Visar hur man slår samman dokument från stream till ett enda utdatadokument.

```csharp
//Det finns flera sätt att slå samman dokument från stream:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveOptions.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveFormat.docx", FileMode.Create, FileAccess.ReadWrite))                    
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        Document doc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        doc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.DocumentInstance.docx");
    }
}
```

### Se även

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namnutrymme [Aspose.Words.LowCode](../../merger/)
* hopsättning [Aspose.Words](../../../)


