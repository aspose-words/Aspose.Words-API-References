---
title: IRevisionCriteria.isMatch method
linktitle: isMatch method
articleTitle: isMatch method
second_title: Aspose.Words for Node.js
description: "IRevisionCriteria.isMatch method. Checks whether or not specified *revision* matches criteria."
type: docs
weight: 10
url: /nodejs-net/aspose.words/irevisioncriteria/isMatch/
---

## isMatch(revision) {#revision}

Checks whether or not specified *revision* matches criteria.


```js
isMatch(revision: Aspose.Words.Revision)
```

| Parameter | Type | Description |
| --- | --- | --- |
| revision | [Revision](../../revision/) | The [Revision](../../revision/) instance to match criteria. |

### Remarks

The method implementation should not accept/reject the revision or modify it in any way due to unexpected results.


### Returns

``True`` if the *revision* matches criteria, otherwise``False``.


### Examples

Shows how to accept or reject revision based on criteria.

```js
test('RevisionSpecifiedCriteria', () => {
  let doc = new aw.Document();
  let builder = new aw.DocumentBuilder(doc);
  builder.write("This does not count as a revision. ");

  // To register our edits as revisions, we need to declare an author, and then start tracking them.
  doc.startTrackRevisions("John Doe", Date.now());            
  builder.write("This is insertion revision #1. ");
  doc.stopTrackRevisions();

  doc.startTrackRevisions("Jane Doe", Date.now());
  builder.write("This is insertion revision #2. ");
  // Remove a run "This does not count as a revision.".
  doc.firstSection.body.firstParagraph.runs.at(0).remove();
  doc.stopTrackRevisions();

  expect(doc.revisions.count).toEqual(3);
  // We have two revisions from different authors, so we need to accept only one.
  doc.revisions.accept(new RevisionCriteria("John Doe", aw.RevisionType.Insertion));
  expect(doc.revisions.count).toEqual(2);
  // Reject revision with different author name and revision type.
  doc.revisions.reject(new RevisionCriteria("Jane Doe", aw.RevisionType.Deletion));
  expect(doc.revisions.count).toEqual(1);

  doc.save(base.artifactsDir + "Revision.RevisionSpecifiedCriteria.docx");
});


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
    return revision.author == AuthorName && revision.revisionType == RevisionType;
  }
}
```

### See Also

* module [Aspose.Words](../../)
* class [IRevisionCriteria](../)

