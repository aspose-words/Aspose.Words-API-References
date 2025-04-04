---
title: Comment.removeAllReplies method
linktitle: removeAllReplies method
articleTitle: removeAllReplies method
second_title: Aspose.Words for Node.js
description: "Comment.removeAllReplies method. Removes all replies to this comment."
type: docs
weight: 170
url: /nodejs-net/aspose.words/comment/removeAllReplies/
---

## removeAllReplies() {#default}

Removes all replies to this comment.


```js
removeAllReplies()
```

### Remarks

All constituent nodes of the replies will be deleted from the document.


### Examples

Shows how to remove comment replies.

```js
let doc = new aw.Document();

let comment = new aw.Comment(doc, "John Doe", "J.D.", Date.now());
comment.setText("My comment.");

doc.firstSection.body.firstParagraph.appendChild(comment);

comment.addReply("Joe Bloggs", "J.B.", Date.now(), "New reply");
comment.addReply("Joe Bloggs", "J.B.", Date.now(), "Another reply");

expect(comment.replies.count).toEqual(2);

// Below are two ways of removing replies from a comment.
// 1 -  Use the "RemoveReply" method to remove replies from a comment individually:
comment.removeReply(comment.replies.at(0));

expect(comment.replies.count).toEqual(1);

// 2 -  Use the "RemoveAllReplies" method to remove all replies from a comment at once:
comment.removeAllReplies();

expect(comment.replies.count).toEqual(0);
```

### See Also

* module [Aspose.Words](../../)
* class [Comment](../)

