---
title: Processor Class
linktitle: Processor
articleTitle: Processor
second_title: Aspose.Words for .NET
description: Enhance document processing with Aspose.Words.LowCode.Processor class, designed for seamless and efficient handling of various document tasks.
type: docs
weight: 4360
url: /net/aspose.words.lowcode/processor/
---
## Processor class

Processor class for performing different document processing actions.

```csharp
public class Processor
```

## Methods

| Name | Description |
| --- | --- |
| [Execute](../../aspose.words.lowcode/processor/execute/#execute)() | Execute the processor action. |
| [Execute](../../aspose.words.lowcode/processor/execute/#execute_1)(*CancellationToken*) | Execute the processor action allowing canceling document processing task using specified cancellation token. |
| [From](../../aspose.words.lowcode/processor/from/#from)(*Stream*) | Specifies input document for processing. |
| [From](../../aspose.words.lowcode/processor/from/#from_2)(*string*) | Specifies input document for processing. |
| [From](../../aspose.words.lowcode/processor/from/#from_1)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Specifies input document for processing. |
| [From](../../aspose.words.lowcode/processor/from/#from_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Specifies input document for processing. |
| [To](../../aspose.words.lowcode/processor/to/#to_4)(*string*) | Specifies output file for the processor. |
| [To](../../aspose.words.lowcode/processor/to/#to)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Specifies output Document streams list. |
| [To](../../aspose.words.lowcode/processor/to/#to_1)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifies output Document streams list. |
| [To](../../aspose.words.lowcode/processor/to/#to_2)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Specifies output stream for the processor. |
| [To](../../aspose.words.lowcode/processor/to/#to_3)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifies output stream for the processor. |
| [To](../../aspose.words.lowcode/processor/to/#to_5)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Specifies output file for the processor. |
| [To](../../aspose.words.lowcode/processor/to/#to_6)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Specifies output file for the processor. |

## Examples

Shows how to convert documents with a single line of code using context.

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

Shows how to do mail merge operation from a DataTable using documents from the stream using context.

```csharp
// There is a several ways to do mail merge operation from a DataTable using documents from the stream:
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

Shows how to convert documents from a stream with a single line of code using context.

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

Shows how to merge documents into a single output document using context.

```csharp
//There is a several ways to merge documents:
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

Shows how to merge documents from stream into a single output document using context.

```csharp
//There is a several ways to merge documents:
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

### See Also

* namespace [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../)
