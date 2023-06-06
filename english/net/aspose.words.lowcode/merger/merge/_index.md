---
title: Merger.Merge
linktitle: Merge
articleTitle: Merge
second_title: Aspose.Words for .NET
description: Merger Merge method. Merges the given input documents into a single output document using specified input and output file names in C#.
type: docs
weight: 10
url: /net/aspose.words.lowcode/merger/merge/
---
## Merge(*string, string[]*) {#merge_4}

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

### See Also

* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../merger/)
* assembly [Aspose.Words](../../../)

---

## Merge(*string, string[], [SaveFormat](../../../aspose.words/saveformat/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_5}

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

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../merger/)
* assembly [Aspose.Words](../../../)

---

## Merge(*string, string[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_6}

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

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../merger/)
* assembly [Aspose.Words](../../../)

---

## Merge(*string[], [MergeFormatMode](../../mergeformatmode/)*) {#merge_1}

Merges the given input documents into a single document and returns [`Document`](../../../aspose.words/document/) instance of the final document.

```csharp
public static Document Merge(string[] inputFiles, MergeFormatMode mergeFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFiles | String[] | The input file names. |
| mergeFormatMode | MergeFormatMode | Specifies how to merge formatting that clashes. |

### See Also

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../merger/)
* assembly [Aspose.Words](../../../)

---

## Merge(*Stream, Stream[], [SaveFormat](../../../aspose.words/saveformat/)*) {#merge_2}

Merges the given input documents into a single output document using specified input output streams and the final document format.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveFormat saveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | Stream | The output stream. |
| inputStreams | Stream[] | The input streams. |
| saveFormat | SaveFormat | The save format. |

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../merger/)
* assembly [Aspose.Words](../../../)

---

## Merge(*Stream, Stream[], [SaveOptions](../../../aspose.words.saving/saveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#merge_3}

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

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../merger/)
* assembly [Aspose.Words](../../../)

---

## Merge(*Stream[], [MergeFormatMode](../../mergeformatmode/)*) {#merge}

Merges the given input documents into a single document and returns [`Document`](../../../aspose.words/document/) instance of the final document.

```csharp
public static Document Merge(Stream[] inputStreams, MergeFormatMode mergeFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStreams | Stream[] | The input streams. |
| mergeFormatMode | MergeFormatMode | Specifies how to merge formatting that clashes. |

### See Also

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../merger/)
* assembly [Aspose.Words](../../../)
