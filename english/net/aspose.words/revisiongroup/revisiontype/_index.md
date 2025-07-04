---
title: RevisionGroup.RevisionType
linktitle: RevisionType
articleTitle: RevisionType
second_title: Aspose.Words for .NET
description: Discover the RevisionGroup RevisionType property to easily identify and manage the types of revisions in your project. Streamline your workflow today!
type: docs
weight: 20
url: /net/aspose.words/revisiongroup/revisiontype/
---
## RevisionGroup.RevisionType property

Gets the type of revisions included in this group.

```csharp
public RevisionType RevisionType { get; }
```

## Examples

Shows how to print info about a group of revisions in a document.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Assert.That(doc.Revisions.Groups.Count, Is.EqualTo(7));

foreach (RevisionGroup group in doc.Revisions.Groups)
{
    Console.WriteLine(
        $"Revision author: {group.Author}; Revision type: {group.RevisionType} \n\tRevision text: {group.Text}");
}
```

### See Also

* enum [RevisionType](../../revisiontype/)
* class [RevisionGroup](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
