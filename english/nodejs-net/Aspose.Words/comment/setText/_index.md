---
title: Comment.setText method
linktitle: setText method
articleTitle: setText method
second_title: Aspose.Words for NodeJs
description: "Comment.setText method. This is a convenience method that allows to easily set text of the comment."
type: docs
weight: 190
url: /nodejs-net/aspose.words/comment/setText/
---

## setText(text) {#string}

This is a convenience method that allows to easily set text of the comment.


```js
setText(text: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | string | The new text of the comment. |

### Remarks

This method allows to quickly set text of a comment from a string. The string can contain
paragraph breaks, this will create paragraphs of text in the comment accordingly.
If you want to insert more complex elements into the comment, for example bookmarks
or tables or apply rich formatting, then you need to use the appropriate node classes to
build up the comment text.




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

