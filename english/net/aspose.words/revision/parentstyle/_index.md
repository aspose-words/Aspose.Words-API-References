---
title: Revision.ParentStyle
linktitle: ParentStyle
second_title: Aspose.Words for .NET API Reference
description: Revision ParentStyle property. Gets the immediate parent style owner of this revision. This property will work for only for the StyleDefinitionChange revision type in C#.
type: docs
weight: 50
url: /net/aspose.words/revision/parentstyle/
---
## Revision.ParentStyle property

Gets the immediate parent style (owner) of this revision. This property will work for only for the StyleDefinitionChange revision type.

```csharp
public Style ParentStyle { get; }
```

## Remarks

If this revision relates to changes on document nodes, use [`ParentNode`](../parentnode/) instead.

## Examples

Shows how to work with a document's collection of revisions.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

// This collection itself has a collection of revision groups.
// Each group is a sequence of adjacent revisions.
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// Iterate over the collection of groups and print the text that the revision concerns.
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// Each Run that a revision affects gets a corresponding Revision object.
// The revisions' collection is considerably larger than the condensed form we printed above,
// depending on how many Runs we have segmented the document into during Microsoft Word editing.
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // A StyleDefinitionChange strictly affects styles and not document nodes. This means the "ParentStyle"
        // property will always be in use, while the ParentNode will always be null.
        // Since all other changes affect nodes, ParentNode will conversely be in use, and ParentStyle will be null.
        if (e.Current.RevisionType == RevisionType.StyleDefinitionChange)
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, style: [{e.Current.ParentStyle.Name}]");
        }
        else
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, contents: [{e.Current.ParentNode.GetText().Trim()}]");
        }
    }
}

// Reject all revisions via the collection, reverting the document to its original form.
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### See Also

* class [Style](../../style/)
* class [Revision](../)
* namespace [Aspose.Words](../../revision/)
* assembly [Aspose.Words](../../../)
