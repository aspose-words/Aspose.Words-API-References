---
title: Document.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words for .NET
description: Document UnlinkFields method. Unlinks fields in the whole document in C#.
type: docs
weight: 770
url: /net/aspose.words/document/unlinkfields/
---
## Document.UnlinkFields method

Unlinks fields in the whole document.

```csharp
public void UnlinkFields()
```

## Remarks

Replaces all the fields in the whole document with their most recent results.

To unlink fields in a specific part of the document use [`UnlinkFields`](../../range/unlinkfields/).

## Examples

Shows how to unlink all fields in the document.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

doc.UnlinkFields();
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
