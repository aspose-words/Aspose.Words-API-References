---
title: Range.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words for .NET
description: Discover the Range UnlinkFields method to effortlessly unlink fields in your document range, enhancing your workflow and document management.
type: docs
weight: 120
url: /net/aspose.words/range/unlinkfields/
---
## Range.UnlinkFields method

Unlinks fields in this range.

```csharp
public void UnlinkFields()
```

## Remarks

Replaces all the fields in this range with their most recent results.

To unlink fields in the whole document use `UnlinkFields`.

## Examples

Shows how to unlink all fields in a range.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

Section newSection = (Section)doc.Sections[0].Clone(true);
doc.Sections.Add(newSection);

doc.Sections[1].Range.UnlinkFields();
```

### See Also

* class [Range](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
