---
title: Document.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words for .NET
description: Discover the Document ExtractPages method to effortlessly retrieve specific page ranges, enhancing your document management and efficiency.
type: docs
weight: 640
url: /net/aspose.words/document/extractpages/
---
## ExtractPages(*int, int, [PageExtractOptions](../../pageextractoptions/)*) {#extractpages_1}

Returns the [`Document`](../) object representing the specified range of pages and the given page extract options.

```csharp
public Document ExtractPages(int index, int count, PageExtractOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | Int32 | The zero-based index of the first page to extract. |
| count | Int32 | Number of pages to be extracted. |
| options | PageExtractOptions | Provides options for managing the page extracting process. |

## Remarks

The resulting document should look like the one in MS Word, as if we had performed 'Print specific pages' – the numbering, headers/footers and cross tables layout will be preserved. But due to a large number of nuances, appearing while reducing the number of pages, full match of the layout is a quiet complicated task requiring a lot of effort. Depending on the document complexity there might be slight differences in the resulting document contents layout comparing to the source document. Any feedback would be greatly appreciated.

### See Also

* class [PageExtractOptions](../../pageextractoptions/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## ExtractPages(*int, int*) {#extractpages}

Returns the [`Document`](../) object representing specified range of pages.

```csharp
public Document ExtractPages(int index, int count)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | Int32 | The zero-based index of the first page to extract. |
| count | Int32 | Number of pages to be extracted. |

## Remarks

The resulting document should look like the one in MS Word, as if we had performed 'Print specific pages' – the numbering, headers/footers and cross tables layout will be preserved. But due to a large number of nuances, appearing while reducing the number of pages, full match of the layout is a quiet complicated task requiring a lot of effort. Depending on the document complexity there might be slight differences in the resulting document contents layout comparing to the source document. Any feedback would be greatly appreciated.

## Examples

Shows how to get specified range of pages from the document.

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

Show how to reset the initial page numbering and save the NUMPAGE field.

```csharp
Document doc = new Document(MyDir + "Page fields.docx");

// Default behavior:
// The extracted page numbering is the same as in the original document, as if we had selected "Print 2 pages" in MS Word.
// The start page will be set to 2 and the field indicating the number of pages will be removed
// and replaced with a constant value equal to the number of pages.
Document extractedDoc1 = doc.ExtractPages(1, 1);
extractedDoc1.Save(ArtifactsDir + "Document.ExtractPagesWithOptions.Default.docx");

// Altered behavior:
// The extracted page numbering is reset and a new one begins,
// as if we had copied the contents of the second page and pasted it into a new document.
// The start page will be set to 1 and the field indicating the number of pages will be left unchanged
// and will show the current number of pages.
PageExtractOptions extractOptions = new PageExtractOptions();
extractOptions.UpdatePageStartingNumber = false;
extractOptions.UnlinkPagesNumberFields = false;
Document extractedDoc2 = doc.ExtractPages(1, 1, extractOptions);
extractedDoc2.Save(ArtifactsDir + "Document.ExtractPagesWithOptions.Options.docx");
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
