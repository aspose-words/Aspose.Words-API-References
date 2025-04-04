---
title: Comparer.CompareToImages
linktitle: CompareToImages
articleTitle: CompareToImages
second_title: Aspose.Words for .NET
description: Effortlessly compare documents with CompareToImages, saving differences as images for each page, enhancing clarity and visual analysis.
type: docs
weight: 30
url: /net/aspose.words.lowcode/comparer/comparetoimages/
---
## CompareToImages(*string, string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages_1}

Compares two documents and saves the differences as images. Each item in the returned array represents a single page of the output rendered as an image.

```csharp
public static Stream[] CompareToImages(string v1, string v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | String | The original document. |
| v2 | String | The modified document. |
| imageSaveOptions | ImageSaveOptions | The output's image save options. |
| author | String | Initials of the author to use for revisions. |
| dateTime | DateTime | The date and time to use for revisions. |
| compareOptions | CompareOptions | Document comparison options. |

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## CompareToImages(*Stream, Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages}

Compares two documents and saves the differences as images. Each item in the returned array represents a single page of the output rendered as an image.

```csharp
public static Stream[] CompareToImages(Stream v1, Stream v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | Stream | The original document. |
| v2 | Stream | The modified document. |
| imageSaveOptions | ImageSaveOptions | The output's image save options. |
| author | String | Initials of the author to use for revisions. |
| dateTime | DateTime | The date and time to use for revisions. |
| compareOptions | CompareOptions | Document comparison options. |

## Examples

Shows how to compare documents and save results as images.

```csharp
// There is a several ways to compare documents:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Stream[] pages = Comparer.CompareToImages(firstDoc, secondDoc, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime());

using (FileStream firstStreamIn = new FileStream(firstDoc, FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(secondDoc, FileMode.Open, FileAccess.Read))
    {
        CompareOptions compareOptions = new CompareOptions();
        compareOptions.IgnoreCaseChanges = true;
        pages = Comparer.CompareToImages(firstStreamIn, secondStreamIn, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime(), compareOptions);
    }
}
```

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
