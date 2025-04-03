---
title: Comment.removeReply method
linktitle: removeReply method
articleTitle: removeReply method
second_title: Aspose.Words for NodeJs
description: "Comment.removeReply method. Removes the specified reply to this comment."
type: docs
weight: 180
url: /nodejs-net/aspose.words/comment/removeReply/
---

## removeReply(reply) {#comment}

Removes the specified reply to this comment.


```js
removeReply(reply: Aspose.Words.Comment)
```

| Parameter | Type | Description |
| --- | --- | --- |
| reply | [Comment](../) | The comment node of the deleting reply. |

### Remarks

All constituent nodes of the reply will be deleted from the document.


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

