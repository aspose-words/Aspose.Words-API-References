---
title: Processor.From
linktitle: From
articleTitle: From
second_title: Aspose.Words for .NET
description: Enhance your workflow with our processor that efficiently handles input documents for seamless processing and improved productivity.
type: docs
weight: 20
url: /net/aspose.words.lowcode/processor/from/
---
## From(*string*) {#from_2}

Specifies input document for processing.

```csharp
public Processor From(string input)
```

| Parameter | Type | Description |
| --- | --- | --- |
| input | String | Input document file name. |

### Return Value

Returns processor with specified input file.

## Remarks

If the processor accepts only one file as an input, only the last specified file will be processed. [`Merger`](../../merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [`Converter`](../../converter/) processor accepts only one file as an input, so only the last specified file will be converted.

### See Also

* class [Processor](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## From(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#from_3}

Specifies input document for processing.

```csharp
public Processor From(string input, LoadOptions loadOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| input | String | Input document file name. |
| loadOptions | LoadOptions | Optional load options used to load the document. |

### Return Value

Returns processor with specified input file.

## Remarks

If the processor accepts only one file as an input, only the last specified file will be processed. [`Merger`](../../merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [`Converter`](../../converter/) processor accepts only one file as an input, so only the last specified file will be converted.

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

### See Also

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Processor](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## From(*Stream*) {#from}

Specifies input document for processing.

```csharp
public Processor From(Stream input)
```

| Parameter | Type | Description |
| --- | --- | --- |
| input | Stream | Input document stream. |

### Return Value

Returns processor with specified input file stream.

## Remarks

If the processor accepts only one file as an input, only the last specified file will be processed. [`Merger`](../../merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [`Converter`](../../converter/) processor accepts only one file as an input, so only the last specified file will be converted.

### See Also

* class [Processor](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## From(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#from_1}

Specifies input document for processing.

```csharp
public Processor From(Stream input, LoadOptions loadOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| input | Stream | Input document stream. |
| loadOptions | LoadOptions | Optional load options used to load the document. |

### Return Value

Returns processor with specified input file stream.

## Remarks

If the processor accepts only one file as an input, only the last specified file will be processed. [`Merger`](../../merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [`Converter`](../../converter/) processor accepts only one file as an input, so only the last specified file will be converted.

## Examples

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

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Processor](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
