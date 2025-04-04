---
title: CommentCollection class
linktitle: CommentCollection class
articleTitle: CommentCollection class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.CommentCollection class. Provides typed access to a collection of [Comment](../comment/) nodes"
type: docs
weight: 200
url: /nodejs-net/aspose.words/commentcollection/
---

## CommentCollection class

Provides typed access to a collection of [Comment](../comment/) nodes.
To learn more, visit the [Working with Comments](https://docs.aspose.com/words/nodejs-net/working-with-comments/) documentation article.




**Inheritance:** [CommentCollection](./) → [NodeCollection](../nodecollection/)

### Properties

| Name | Description |
| --- | --- |
| [count](../nodecollection/count/) | Gets the number of nodes in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
| [this[]](../nodecollection/this[]/) | <br>(Inherited from [NodeCollection](../nodecollection/)) |

### Methods

| Name | Description |
| --- | --- |
|[ add(node)](../nodecollection/add/#node) | Adds a node to the end of the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ clear()](../nodecollection/clear/#default) | Removes all nodes from this collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ contains(node)](../nodecollection/contains/#node) | Determines whether a node is in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ indexOf(node)](../nodecollection/indexOf/#node) | Returns the zero-based index of the specified node.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ insert(index, node)](../nodecollection/insert/#number_node) | Inserts a node into the collection at the specified index.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ remove(node)](../nodecollection/remove/#node) | Removes the node from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ removeAt(index)](../nodecollection/removeAt/#number) | Removes the node at the specified index from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ toArray()](../nodecollection/toArray/#default) | Copies all nodes from the collection to a new array of nodes.<br>(Inherited from [NodeCollection](../nodecollection/)) |

### Examples

Shows how to mark a comment as "done".

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Helo world!");

// Insert a comment to point out an error. 
let comment = new aw.Comment(doc, "John Doe", "J.D.", Date.now());
comment.setText("Fix the spelling error!");
doc.firstSection.body.firstParagraph.appendChild(comment);

// Comments have a "Done" flag, which is set to "false" by default. 
// If a comment suggests that we make a change within the document,
// we can apply the change, and then also set the "Done" flag afterwards to indicate the correction.
expect(comment.done).toEqual(false);

doc.firstSection.body.firstParagraph.runs.at(0).text = "Hello world!";
comment.done = true;

// Comments that are "done" will differentiate themselves
// from ones that are not "done" with a faded text color.
comment = new aw.Comment(doc, "John Doe", "J.D.", Date.now());
comment.setText("Add text to this paragraph.");
builder.currentParagraph.appendChild(comment);

doc.save(base.artifactsDir + "Comment.done.docx");
```

### See Also

* module [Aspose.Words](../)
* class [NodeCollection](../nodecollection/)

