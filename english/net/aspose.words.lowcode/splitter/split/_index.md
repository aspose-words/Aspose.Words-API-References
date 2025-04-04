---
title: Splitter.Split
linktitle: Split
articleTitle: Split
second_title: Aspose.Words for .NET
description: Effortlessly split documents into multiple sections with our flexible Splitter Split method. Save in your preferred format for easy file management!
type: docs
weight: 40
url: /net/aspose.words.lowcode/splitter/split/
---
## Split(*string, string, [SplitOptions](../../splitoptions/)*) {#split_2}

Splits a document into multiple parts based on the specified split options and saves the resulting parts to files. The output file format is determined by the extension of the output file name.

```csharp
public static void Split(string inputFileName, string outputFileName, SplitOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name used to generate file name for document parts using rule "outputFile_partIndex.extension" |
| options | SplitOptions | Document split options. |

## Examples

Shows how to split document by pages.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### See Also

* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Split(*string, string, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split_3}

Splits a document into multiple parts based on the specified split options and saves the resulting parts to files in the specified save format.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    SplitOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name used to generate file name for document parts using rule "outputFile_partIndex.extension" |
| saveFormat | SaveFormat | The save format. |
| options | SplitOptions | Document split options. |

## Examples

Shows how to split document by pages.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Split(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_4}

Splits a document into multiple parts based on the specified split options and saves the resulting parts to files in the specified save format.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    SplitOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name used to generate file name for document parts using rule "outputFile_partIndex.extension" |
| saveOptions | SaveOptions | The save options. |
| options | SplitOptions | Document split options. |

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Split(*Stream, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split}

Splits a document from an input stream into multiple parts based on the specified split options and returns the resulting parts as an array of streams in the specified save format.

```csharp
public static Stream[] Split(Stream inputStream, SaveFormat saveFormat, SplitOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input stream. |
| saveFormat | SaveFormat | The save format. |
| options | SplitOptions | Document split options. |

## Examples

Shows how to split document from the stream by pages.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitOptions options = new SplitOptions();
    options.SplitCriteria = SplitCriteria.Page;
    Stream[] stream = Splitter.Split(streamIn, SaveFormat.Docx, options);
}
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Split(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_1}

Splits a document from an input stream into multiple parts based on the specified split options and returns the resulting parts as an array of streams in the specified save format.

```csharp
public static Stream[] Split(Stream inputStream, SaveOptions saveOptions, SplitOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input stream. |
| saveOptions | SaveOptions | The save options. |
| options | SplitOptions | Document split options. |

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
