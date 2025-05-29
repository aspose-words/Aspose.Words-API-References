---
title: Processor Class
linktitle: Processor
articleTitle: Processor
second_title: Aspose.Words för .NET
description: Förbättra dokumenthanteringen med klassen Aspose.Words.LowCode.Processor, utformad för sömlös och effektiv hantering av olika dokumentuppgifter.
type: docs
weight: 4320
url: /sv/net/aspose.words.lowcode/processor/
---
## Processor class

Processorklass för att utföra olika dokumentbehandlingsåtgärder.

```csharp
public class Processor
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Utför processoråtgärden. |
| [From](../../aspose.words.lowcode/processor/from/#from)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Anger indatadokument för bearbetning. |
| [From](../../aspose.words.lowcode/processor/from/#from_1)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Anger indatadokument för bearbetning. |
| [To](../../aspose.words.lowcode/processor/to/#to)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Anger listan över utdatadokumentströmmar. |
| [To](../../aspose.words.lowcode/processor/to/#to_1)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Anger listan över utdatadokumentströmmar. |
| [To](../../aspose.words.lowcode/processor/to/#to_2)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Anger utdataströmmen för processorn. |
| [To](../../aspose.words.lowcode/processor/to/#to_3)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Anger utdataströmmen för processorn. |
| [To](../../aspose.words.lowcode/processor/to/#to_4)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Anger utdatafilen för processorn. |
| [To](../../aspose.words.lowcode/processor/to/#to_5)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Anger utdatafilen för processorn. |

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

Visar hur man utför en dokumentkopplingsoperation från en datatabell med hjälp av dokument från strömmen med hjälp av kontext.

```csharp
// Det finns flera sätt att göra en dokumentkopplingsoperation från en datatabell med hjälp av dokument från strömmen:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(dataTable);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamDataTable.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

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

* namnutrymme [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../)
