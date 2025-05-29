---
title: Processor.To
linktitle: To
articleTitle: To
second_title: Aspose.Words för .NET
description: Optimera ditt arbetsflöde med vår processormetod som tydligt definierar utdatafiler, vilket ökar effektiviteten och effektiviserar dina datahanteringsuppgifter.
type: docs
weight: 30
url: /sv/net/aspose.words.lowcode/processor/to/
---
## To(*string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_5}

Anger utdatafilen för processorn.

```csharp
public Processor To(string output, SaveOptions saveOptions = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| output | String | Namn på utdatafil. |
| saveOptions | SaveOptions | Valfria sparalternativ. Om inget anges bestäms sparformatet av filändelsen. |

### Returvärde

Returnerar processorn med den specificerade utdatafilen.

## Anmärkningar

Om utdata består av flera filer används det angivna utdatafilnamnet för att generera filnamnet för varje del enligt regeln: 'outputFile_partIndex.extension'.

## Exempel

Visar hur man konverterar dokument med en enda kodrad med hjälp av kontext.

```csharp
string doc = MyDir + "Big document.docx";

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.1.pdf")
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.2.pdf", SaveFormat.Rtf)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Create(new ConverterContext())
    .From(doc, loadOptions)
    .To(ArtifactsDir + "LowCode.ConvertContext.3.docx", saveOptions)
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.Png))
    .Execute();
```

Visar hur man sammanfogar dokument till ett enda utdatadokument med hjälp av kontext.

```csharp
//Det finns flera sätt att sammanfoga dokument:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.1.docx")
    .Execute();

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1, firstLoadOptions)
    .From(inputDoc2, secondLoadOptions)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.2.docx", SaveFormat.Docx)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.3.docx", saveOptions)
    .Execute();
```

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## To(*string, [SaveFormat](../../../aspose.words/saveformat/)*) {#to_4}

Anger utdatafilen för processorn.

```csharp
public Processor To(string output, SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| output | String | Namn på utdatafil. |
| saveFormat | SaveFormat | Sparformat. Om inget anges bestäms sparformatet av filändelsen. |

### Returvärde

Returnerar processorn med den specificerade utdatafilen.

## Anmärkningar

Om utdata består av flera filer används det angivna utdatafilnamnet för att generera filnamnet för varje del enligt regeln: 'outputFile_partIndex.extension'.

## Exempel

Visar hur man sammanfogar dokument till ett enda utdatadokument med hjälp av kontext.

```csharp
//Det finns flera sätt att sammanfoga dokument:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.1.docx")
    .Execute();

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1, firstLoadOptions)
    .From(inputDoc2, secondLoadOptions)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.2.docx", SaveFormat.Docx)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.3.docx", saveOptions)
    .Execute();
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## To(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_3}

Anger utdataströmmen för processorn.

```csharp
public Processor To(Stream output, SaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| output | Stream | Utgångsström. |
| saveOptions | SaveOptions | Spara alternativ. |

### Returvärde

Returnerar processor med specificerad utdataström.

## Anmärkningar

Om utdata består av flera filer sparas endast den första delen i den angivna strömmen.

## Exempel

Visar hur man konverterar dokument från en ström med en enda kodrad med hjälp av kontext.

```csharp
string doc = MyDir + "Document.docx";
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn)
            .To(streamOut, SaveFormat.Rtf)
            .Execute();

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn, loadOptions)
            .To(streamOut, saveOptions)
            .Execute();

    List<Stream> pages = new List<Stream>();
    Converter.Create(new ConverterContext())
        .From(doc)
        .To(pages, new ImageSaveOptions(SaveFormat.Png))
        .Execute();
}
```

Visar hur man sammanfogar dokument från en ström till ett enda utdatadokument med hjälp av kontext.

```csharp
//Det finns flera sätt att sammanfoga dokument:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn)
            .From(secondStreamIn)
            .To(streamOut, saveOptions)
            .Execute();

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn, firstLoadOptions)
            .From(secondStreamIn, secondLoadOptions)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
    }
}
```

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## To(*Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#to_2}

Anger utdataströmmen för processorn.

```csharp
public Processor To(Stream output, SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| output | Stream | Utgångsström. |
| saveFormat | SaveFormat | Spara format. |

### Returvärde

Returnerar processor med specificerad utdataström.

## Anmärkningar

Om utdata består av flera filer sparas endast den första delen i den angivna strömmen.

## Exempel

Visar hur man konverterar dokument från en ström med en enda kodrad med hjälp av kontext.

```csharp
string doc = MyDir + "Document.docx";
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn)
            .To(streamOut, SaveFormat.Rtf)
            .Execute();

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn, loadOptions)
            .To(streamOut, saveOptions)
            .Execute();

    List<Stream> pages = new List<Stream>();
    Converter.Create(new ConverterContext())
        .From(doc)
        .To(pages, new ImageSaveOptions(SaveFormat.Png))
        .Execute();
}
```

Visar hur man sammanfogar dokument från en ström till ett enda utdatadokument med hjälp av kontext.

```csharp
//Det finns flera sätt att sammanfoga dokument:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn)
            .From(secondStreamIn)
            .To(streamOut, saveOptions)
            .Execute();

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn, firstLoadOptions)
            .From(secondStreamIn, secondLoadOptions)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
    }
}
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## To(*List&lt;Stream&gt;, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#to_1}

Anger listan över utdatadokumentströmmar.

```csharp
public Processor To(List<Stream> output, SaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| output | List`1 | Lista över utdatadokumentströmmar. |
| saveOptions | SaveOptions | Spara alternativ. |

### Returvärde

Returnerar processor med angiven lista över utdatadokumentströmmar.

## Anmärkningar

Om utdata består av flera filer (t.ex. bilder eller delade dokumentdelar) läggs en ström för varje del till i den angivna listan. Om utdata är en enda fil läggs endast en ström till i listan. Det är slutanvändarens ansvar att kassera de skapade strömmarna.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Processor](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## To(*List&lt;Stream&gt;, [SaveFormat](../../../aspose.words/saveformat/)*) {#to}

Anger listan över utdatadokumentströmmar.

```csharp
public Processor To(List<Stream> output, SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| output | List`1 | Lista över utdatadokumentströmmar. |
| saveFormat | SaveFormat | Spara format. |

### Returvärde

Returnerar processor med angiven lista över utdatadokumentströmmar.

## Anmärkningar

Om utdata består av flera filer (t.ex. bilder eller delade dokumentdelar) läggs en ström för varje del till i den angivna listan. Om utdata är en enda fil läggs endast en ström till i listan. Det är slutanvändarens ansvar att kassera de skapade strömmarna.

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Processor](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
