---
title: Splitter.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words for .NET
description: Splitter RemoveBlankPages method. Removes empty pages from the document and saves the output. Returns a list of page numbers that were removed in C#.
type: docs
weight: 20
url: /net/aspose.words.lowcode/splitter/removeblankpages/
---
## RemoveBlankPages(*string, string*) {#removeblankpages_2}

Removes empty pages from the document and saves the output. Returns a list of page numbers that were removed.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |

### Return Value

List of page numbers has been considered as blank and removed.

## Examples

Shows how to remove empty pages from the document.

```csharp
// There is a several ways to remove empty pages from the document:
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### See Also

* class [Splitter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages_3}

Removes empty pages from the document and saves the output in the specified format. Returns a list of page numbers that were removed.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveFormat saveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |
| saveFormat | SaveFormat | The save format. |

### Return Value

List of page numbers has been considered as blank and removed.

## Examples

Shows how to remove empty pages from the document.

```csharp
// There is a several ways to remove empty pages from the document:
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_4}

Removes empty pages from the document and saves the output in the specified format. Returns a list of page numbers that were removed.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |
| saveOptions | SaveOptions | The save options. |

### Return Value

List of page numbers has been considered as blank and removed.

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages}

Removes blank pages from a document provided in an input stream and saves the updated document to an output stream in the specified save format. Returns a list of page numbers that were removed.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input stream. |
| outputStream | Stream | The output stream. |
| saveFormat | SaveFormat | The save format. |

### Return Value

List of page numbers has been considered as blank and removed.

## Examples

Shows how to remove empty pages from the document from the stream.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Blank pages.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.RemoveBlankPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.RemoveBlankPages(streamIn, streamOut, SaveFormat.Docx);
}
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_1}

Removes blank pages from a document provided in an input stream and saves the updated document to an output stream in the specified save format. Returns a list of page numbers that were removed.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input stream. |
| outputStream | Stream | The output stream. |
| saveOptions | SaveOptions | The save options. |

### Return Value

List of page numbers has been considered as blank and removed.

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
