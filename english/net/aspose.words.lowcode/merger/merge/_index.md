---
title: Merger.Merge
linktitle: Merge
articleTitle: Merge
second_title: Aspose.Words for .NET
description: Effortlessly combine multiple documents into one with our Merger Merge method. Streamline your workflow with customizable file options today!
type: docs
weight: 10
url: /net/aspose.words.lowcode/merger/merge/
---
## Merge(*string, string[]*) {#merge_8}

Merges the given input documents into a single output document using specified input and output file names.

```csharp
public static void Merge(string outputFile, string[] inputFiles)
```

| Parameter | Type | Description |
| --- | --- | --- |
| outputFile | String | The output file name. |
| inputFiles | String[] | The input file names. |

## Remarks

By default KeepSourceFormatting is used.

## Examples

Shows how to merge documents into a single output document.

```csharp
//There is a several ways to merge documents:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### See Also

* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Merge(*string, string[], [SaveFormat](../../../aspose.words/saveformat/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_10}

Merges the given input documents into a single output document using specified input output file names and the final document format.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveFormat saveFormat, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| outputFile | String | The output file name. |
| inputFiles | String[] | The input file names. |
| saveFormat | SaveFormat | The save format. |
| mergeFormatMode | MergeFormatMode | Specifies how to merge formatting that clashes. |

## Examples

Shows how to merge documents into a single output document.

```csharp
//There is a several ways to merge documents:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Merge(*string, string[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_11}

Merges the given input documents into a single output document using specified input output file names and save options.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| outputFile | String | The output file name. |
| inputFiles | String[] | The input file names. |
| saveOptions | SaveOptions | The save options. |
| mergeFormatMode | MergeFormatMode | Specifies how to merge formatting that clashes. |

## Examples

Shows how to merge documents into a single output document.

```csharp
//There is a several ways to merge documents:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Merge(*string, string[], LoadOptions[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_9}

Merges the given input documents into a single output document using specified input output file names and save options.

```csharp
public static void Merge(string outputFile, string[] inputFiles, LoadOptions[] loadOptions, 
    SaveOptions saveOptions, MergeFormatMode mergeFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| outputFile | String | The output file name. |
| inputFiles | String[] | The input file names. |
| loadOptions | LoadOptions[] | Load options for the input files. |
| saveOptions | SaveOptions | The save options. |
| mergeFormatMode | MergeFormatMode | Specifies how to merge formatting that clashes. |

## Examples

Shows how to merge documents into a single output document.

```csharp
//There is a several ways to merge documents:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### See Also

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Merge(*string[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_4}

Merges the given input documents into a single document and returns [`Document`](../../../aspose.words/document/) instance of the final document.

```csharp
public static Document Merge(string[] inputFiles, MergeFormatMode mergeFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFiles | String[] | The input file names. |
| mergeFormatMode | MergeFormatMode | Specifies how to merge formatting that clashes. |

## Examples

Shows how to merge documents into a single output document.

```csharp
//There is a several ways to merge documents:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### See Also

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Merge(*string[], LoadOptions[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_3}

Merges the given input documents into a single document and returns [`Document`](../../../aspose.words/document/) instance of the final document.

```csharp
public static Document Merge(string[] inputFiles, LoadOptions[] loadOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFiles | String[] | The input file names. |
| loadOptions | LoadOptions[] | Load options for the input files. |
| mergeFormatMode | MergeFormatMode | Specifies how to merge formatting that clashes. |

## Examples

Shows how to merge documents into a single output document.

```csharp
//There is a several ways to merge documents:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### See Also

* class [Document](../../../aspose.words/document/)
* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Merge(*Document[], [MergeFormatMode](../../mergeformatmode/)*) {#merge}

Merges the given input documents into a single document and returns [`Document`](../../../aspose.words/document/) instance of the final document.

```csharp
public static Document Merge(Document[] inputDocuments, MergeFormatMode mergeFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputDocuments | Document[] | The input documents. |
| mergeFormatMode | MergeFormatMode | Specifies how to merge formatting that clashes. |

## Examples

Shows how to merge input documents to a single document instance.

```csharp
DocumentBuilder firstDoc = new DocumentBuilder();
firstDoc.Font.Size = 16;
firstDoc.Font.Color = Color.Blue;
firstDoc.Write("Hello first word!");

DocumentBuilder secondDoc = new DocumentBuilder();
secondDoc.Write("Hello second word!");

Document mergedDoc = Merger.Merge(new Document[] { firstDoc.Document, secondDoc.Document }, MergeFormatMode.KeepSourceLayout);
Assert.AreEqual("Hello first word!\fHello second word!\f", mergedDoc.GetText());
```

### See Also

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Merge(*Stream, Stream[], [SaveFormat](../../../aspose.words/saveformat/)*) {#merge_6}

Merges the given input documents into a single output document using specified input output streams and the final document format.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveFormat saveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | Stream | The output stream. |
| inputStreams | Stream[] | The input streams. |
| saveFormat | SaveFormat | The save format. |

## Examples

Shows how to merge documents from stream into a single output document.

```csharp
//There is a several ways to merge documents from stream:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Merge(*Stream, Stream[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_7}

Merges the given input documents into a single output document using specified input output streams and save options.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | Stream | The output stream. |
| inputStreams | Stream[] | The input streams. |
| saveOptions | SaveOptions | The save options. |
| mergeFormatMode | MergeFormatMode | Specifies how to merge formatting that clashes. |

## Examples

Shows how to merge documents from stream into a single output document.

```csharp
//There is a several ways to merge documents from stream:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Merge(*Stream, Stream[], LoadOptions[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_5}

Merges the given input documents into a single output document using specified input output streams and save options.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, LoadOptions[] loadOptions, 
    SaveOptions saveOptions, MergeFormatMode mergeFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | Stream | The output stream. |
| inputStreams | Stream[] | The input streams. |
| loadOptions | LoadOptions[] | Load options for the input files. |
| saveOptions | SaveOptions | The save options. |
| mergeFormatMode | MergeFormatMode | Specifies how to merge formatting that clashes. |

## Examples

Shows how to merge documents from stream into a single output document.

```csharp
//There is a several ways to merge documents from stream:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### See Also

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Merge(*Stream[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_2}

Merges the given input documents into a single document and returns [`Document`](../../../aspose.words/document/) instance of the final document.

```csharp
public static Document Merge(Stream[] inputStreams, MergeFormatMode mergeFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStreams | Stream[] | The input streams. |
| mergeFormatMode | MergeFormatMode | Specifies how to merge formatting that clashes. |

## Examples

Shows how to merge documents from stream into a single output document.

```csharp
//There is a several ways to merge documents from stream:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### See Also

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Merge(*Stream[], LoadOptions[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_1}

Merges the given input documents into a single document and returns [`Document`](../../../aspose.words/document/) instance of the final document.

```csharp
public static Document Merge(Stream[] inputStreams, LoadOptions[] loadOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStreams | Stream[] | The input streams. |
| loadOptions | LoadOptions[] | Load options for the input files. |
| mergeFormatMode | MergeFormatMode | Specifies how to merge formatting that clashes. |

## Examples

Shows how to merge documents from stream into a single output document.

```csharp
//There is a several ways to merge documents from stream:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.3.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

        Document firstDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        firstDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.4.docx");

        Document secondDoc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
        secondDoc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.5.docx");
    }
}
```

### See Also

* class [Document](../../../aspose.words/document/)
* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
