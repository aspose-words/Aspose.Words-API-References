---
title: IRevisionCriteria Interface
linktitle: IRevisionCriteria
articleTitle: IRevisionCriteria
second_title: Aspose.Words for .NET
description: Aspose.Words.IRevisionCriteria interface. Implement this interface if you want to control when certain Revision should be accepted/rejected or not by the Accept/Reject methods in C#.
type: docs
weight: 3500
url: /net/aspose.words/irevisioncriteria/
---
## IRevisionCriteria interface

Implement this interface if you want to control when certain [`Revision`](../revision/) should be accepted/rejected or not by the [`Accept`](../revisioncollection/accept/)/[`Reject`](../revisioncollection/reject/) methods.

```csharp
public interface IRevisionCriteria
```

## Methods

| Name | Description |
| --- | --- |
| [IsMatch](../../aspose.words/irevisioncriteria/ismatch/)(*[Revision](../revision/)*) | Checks whether or not specified *revision* matches criteria. |

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

    Assert.AreEqual(3, doc.Revisions.Count);
    // We have two revisions from different authors, so we need to accept only one.
    doc.Revisions.Accept(new RevisionCriteria("John Doe", RevisionType.Insertion));
    Assert.AreEqual(2, doc.Revisions.Count);
    // Reject revision with different author name and revision type.
    doc.Revisions.Reject(new RevisionCriteria("Jane Doe", RevisionType.Deletion));
    Assert.AreEqual(1, doc.Revisions.Count);

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
