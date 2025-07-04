---
title: RevisionCollection.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words for .NET
description: Discover the RevisionCollection Accept method to easily manage and filter revisions based on your criteria for streamlined project updates.
type: docs
weight: 40
url: /net/aspose.words/revisioncollection/accept/
---
## RevisionCollection.Accept method

Accepts revisions that match specified criteria.

```csharp
public int Accept(IRevisionCriteria criteria)
```

| Parameter | Type | Description |
| --- | --- | --- |
| criteria | IRevisionCriteria | The [`IRevisionCriteria`](../../irevisioncriteria/) implementation. |

### Return Value

The count of accepted revisions.

## Examples

Shows how to accept or reject revision based on criteria.

```csharp
public void RevisionSpecifiedCriteria()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Write("This does not count as a revision. ");

    // To register our edits as revisions, we need to declare an author, and then start tracking them.
    doc.StartTrackRevisions("John Doe", DateTime.Now);
    builder.Write("This is insertion revision #1. ");
    doc.StopTrackRevisions();

    doc.StartTrackRevisions("Jane Doe", DateTime.Now);
    builder.Write("This is insertion revision #2. ");
    // Remove a run "This does not count as a revision.".
    doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();
    doc.StopTrackRevisions();

    Assert.That(doc.Revisions.Count, Is.EqualTo(3));
    // We have two revisions from different authors, so we need to accept only one.
    doc.Revisions.Accept(new RevisionCriteria("John Doe", RevisionType.Insertion));
    Assert.That(doc.Revisions.Count, Is.EqualTo(2));
    // Reject revision with different author name and revision type.
    doc.Revisions.Reject(new RevisionCriteria("Jane Doe", RevisionType.Deletion));
    Assert.That(doc.Revisions.Count, Is.EqualTo(1));

    doc.Save(ArtifactsDir + "Revision.RevisionSpecifiedCriteria.docx");
}

/// <summary>
/// Control when certain revision should be accepted/rejected.
/// </summary>
public class RevisionCriteria : IRevisionCriteria
{
    private readonly string AuthorName;
    private readonly RevisionType RevisionType;

    public RevisionCriteria(string authorName, RevisionType revisionType)
    {
        AuthorName = authorName;
        RevisionType = revisionType;
    }

    public bool IsMatch(Revision revision)
    {
        return revision.Author == AuthorName && revision.RevisionType == RevisionType;
    }
}
```

### See Also

* interface [IRevisionCriteria](../../irevisioncriteria/)
* class [RevisionCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
