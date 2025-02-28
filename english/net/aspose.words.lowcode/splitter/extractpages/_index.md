---
title: Splitter.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words for .NET
description: Effortlessly extract specific pages from any document with our Splitter ExtractPages method. Save them in your desired format for easy access!
type: docs
weight: 10
url: /net/aspose.words.lowcode/splitter/extractpages/
---
## ExtractPages(*string, string, int, int*) {#extractpages_4}

Extracts a specified range of pages from a document file and saves the extracted pages to a new file. The output file format is determined by the extension of the output file name.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, int startPageIndex, 
    int pageCount)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |
| startPageIndex | Int32 | The zero-based index of the first page to extract. |
| pageCount | Int32 | Number of pages to be extracted. |

## Examples

Shows how to extract pages from the document.

```csharp
// There is a several ways to extract pages from the document:
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### See Also

* class [Splitter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages_2}

Extracts a specified range of pages from a document file and saves the extracted pages to a new file using the specified save format.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |
| saveFormat | SaveFormat | The save format. |
| startPageIndex | Int32 | The zero-based index of the first page to extract. |
| pageCount | Int32 | Number of pages to be extracted. |

## Examples

Shows how to extract pages from the document.

```csharp
// There is a several ways to extract pages from the document:
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_3}

Extracts a specified range of pages from a document file and saves the extracted pages to a new file using the specified save format.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, int startPageIndex, int pageCount)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |
| saveOptions | SaveOptions | The save options. |
| startPageIndex | Int32 | The zero-based index of the first page to extract. |
| pageCount | Int32 | Number of pages to be extracted. |

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages}

Extracts a specified range of pages from a document stream and saves the extracted pages to an output stream using the specified save format.

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input stream. |
| outputStream | Stream | The output stream. |
| saveFormat | SaveFormat | The save format. |
| startPageIndex | Int32 | The zero-based index of the first page to extract. |
| pageCount | Int32 | Number of pages to be extracted. |

## Examples

Shows how to extract pages from the document from the stream.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ExtractPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.ExtractPages(streamIn, streamOut, SaveFormat.Docx, 0, 2);
}
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_1}

Extracts a specified range of pages from a document stream and saves the extracted pages to an output stream using the specified save format.

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    int startPageIndex, int pageCount)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input stream. |
| outputStream | Stream | The output stream. |
| saveOptions | SaveOptions | The save options. |
| startPageIndex | Int32 | The zero-based index of the first page to extract. |
| pageCount | Int32 | Number of pages to be extracted. |

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
