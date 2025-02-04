---
title: StructuredDocumentTagCollection Class
linktitle: StructuredDocumentTagCollection
articleTitle: StructuredDocumentTagCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Markup.StructuredDocumentTagCollection class. A collection of IStructuredDocumentTag instances that represent the structured document tags in the specified range in C#.
type: docs
weight: 4620
url: /net/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class

A collection of [`IStructuredDocumentTag`](../istructureddocumenttag/) instances that represent the structured document tags in the specified range.

To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/net/working-with-content-control-sdt/) documentation article.

```csharp
public class StructuredDocumentTagCollection : IEnumerable<IStructuredDocumentTag>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.markup/structureddocumenttagcollection/count/) { get; } | Returns the number of structured document tags in the collection. |
| [Item](../../aspose.words.markup/structureddocumenttagcollection/item/) { get; } | Returns the structured document tag at the specified index. |

## Methods

| Name | Description |
| --- | --- |
| [GetById](../../aspose.words.markup/structureddocumenttagcollection/getbyid/)(*int*) | Returns the structured document tag by identifier. |
| [GetByTag](../../aspose.words.markup/structureddocumenttagcollection/getbytag/)(*string*) | Returns the first structured document tag encountered in the collection with the specified tag. |
| [GetByTitle](../../aspose.words.markup/structureddocumenttagcollection/getbytitle/)(*string*) | Returns the first structured document tag encountered in the collection with the specified title. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagcollection/getenumerator/)() | Returns an enumerator object. |
| [Remove](../../aspose.words.markup/structureddocumenttagcollection/remove/)(*int*) | Removes the structured document tag with the specified identifier. |
| [RemoveAt](../../aspose.words.markup/structureddocumenttagcollection/removeat/)(*int*) | Removes a structured document tag at the specified index. |

## Examples

Shows how to get structured document tag.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Get the structured document tag by Id.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// Get the structured document tag or ranged tag by Title.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### See Also

* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* namespace [Aspose.Words.Markup](../../aspose.words.markup/)
* assembly [Aspose.Words](../../)
