---
title: Merger.MergeToImages
linktitle: MergeToImages
articleTitle: MergeToImages
second_title: Aspose.Words for .NET
description: Merge multiple documents effortlessly with the MergeToImages method, creating a single image output while customizing file names and save options.
type: docs
weight: 30
url: /net/aspose.words.lowcode/merger/mergetoimages/
---
## MergeToImages(*string[], [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#mergetoimages_1}

Merges the given input documents into a single output document using specified input output file names and save options. Renders the output to images.

```csharp
public static Stream[] MergeToImages(string[] inputFiles, ImageSaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFiles | String[] | The input file names. |
| saveOptions | ImageSaveOptions | The save options. |
| mergeFormatMode | MergeFormatMode | Specifies how to merge formatting that clashes. |

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## MergeToImages(*Stream[], [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#mergetoimages}

Merges the given input document streams into a single output document using specified image save options. Renders the output to images.

```csharp
public static Stream[] MergeToImages(Stream[] inputStreams, ImageSaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStreams | Stream[] | The input file streams. |
| saveOptions | ImageSaveOptions | The save options. |
| mergeFormatMode | MergeFormatMode | Specifies how to merge formatting that clashes. |

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
