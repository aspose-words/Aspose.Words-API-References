﻿---
title: Comment.author property
linktitle: author property
articleTitle: author property
second_title: Aspose.Words for Node.js
description: "Comment.author property. Returns or sets the author name for a comment."
type: docs
weight: 30
url: /nodejs-net/aspose.words/comment/author/
---

## Comment.author property

Returns or sets the author name for a comment.


```js
get author(): string
```

### Remarks

Cannot be ``null``.

Default is empty string.




### Examples

Shows how to print all of a document's comments and their replies.

```js
let doc = new aw.Document(base.myDir + "Comments.docx");

let comments = [...doc.getChildNodes(aw.NodeType.Comment, true)];
expect(comments.length).toEqual(12);

// If a comment has no ancestor, it is a "top-level" comment as opposed to a reply-type comment.
// Print all top-level comments along with any replies they may have.
for (var node of comments.filter(n => n.ancestor == null))
{
  let comment = node.asComment();
  console.log("Top-level comment:");
  console.log(`\t\"${comment.getText().trim()}\", by ${comment.author}`);
  console.log(`Has ${comment.replies.count} replies`);
  for (let commentReply of comment.replies)
  {
    console.log(`\t\"${commentReply.getText().trim()}\", by ${commentReply.author}`);
  }
  console.log();
}
```

### See Also

* module [Aspose.Words](../../)
* class [Comment](../)

