---
title: Comment.addReply method
linktitle: addReply method
articleTitle: addReply method
second_title: Aspose.Words for NodeJs
description: "Comment.addReply method. Adds a reply to this comment."
type: docs
weight: 160
url: /nodejs-net/Aspose.Words/comment/addReply/
---

## addReply(author, initial, dateTime, text) {#string_string_date_string}

Adds a reply to this comment.


```js
addReply(author: stringinitial: stringdateTime: Datetext: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| author | string | The author name for the reply. |
| initial | string | The author initials for the reply. |
| dateTime | Date | The date and time for the reply. |
| text | string | The reply text. |

### Remarks

Due to the existing MS Office limitations only 1 level of replies is allowed in the document.




### Returns

The created [Comment](../) node for the reply.


### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidOperationException)) | Throws if this method is called on the existing Reply comment. |

### Examples

Shows how to add a comment to a document, and then reply to it.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let comment = new aw.Comment(doc, "John Doe", "J.D.", Date.now());
comment.setText("My comment.");

// Place the comment at a node in the document's body.
// This comment will show up at the location of its paragraph,
// outside the right-side margin of the page, and with a dotted line connecting it to its paragraph.
builder.currentParagraph.appendChild(comment);

// Add a reply, which will show up under its parent comment.
comment.addReply("Joe Bloggs", "J.B.", Date.now(), "New reply");

// Comments and replies are both Comment nodes.
expect(doc.getChildNodes(aw.NodeType.Comment, true).count).toEqual(2);

// Comments that do not reply to other comments are "top-level". They have no ancestor comments.
expect(comment.ancestor).toBe(null);

// Replies have an ancestor top-level comment.
expect(comment.replies.at(0).ancestor).toEqual(comment);

doc.save(base.artifactsDir + "Comment.AddCommentWithReply.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Comment](../)

