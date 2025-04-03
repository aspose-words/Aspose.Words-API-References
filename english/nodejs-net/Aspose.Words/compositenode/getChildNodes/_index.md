---
title: CompositeNode.getChildNodes method
linktitle: getChildNodes method
articleTitle: getChildNodes method
second_title: Aspose.Words for NodeJs
description: "CompositeNode.getChildNodes method. Returns a live collection of child nodes that match the specified type."
type: docs
weight: 110
url: /nodejs-net/Aspose.Words/compositenode/getChildNodes/
---

## getChildNodes(nodeType, isDeep) {#nodetype_boolean}

Returns a live collection of child nodes that match the specified type.


```js
getChildNodes(nodeType: Aspose.Words.NodeTypeisDeep: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | [NodeType](../../nodetype/) | Specifies the type of nodes to select. |
| isDeep | boolean | ``true`` to select from all child nodes recursively; ``false`` to select only among immediate children.  |

### Remarks

The collection of nodes returned by this method is always live.




A live collection is always in sync with the document. For example, if you
selected all sections in a document and enumerate through the collection
deleting the sections, the section is removed from the collection immediately
when it is removed from the document.




### Returns

A live collection of child nodes of the specified type.


### Examples

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```js
let doc = new aw.Document();

// An empty document, by default, has one paragraph.
expect(doc.firstSection.body.paragraphs.count).toEqual(1);

// Composite nodes such as our paragraph can contain other composite and inline nodes as children.
let paragraph = doc.firstSection.body.firstParagraph;
let paragraphText = new aw.Run(doc, "Initial text. ");
paragraph.appendChild(paragraphText);

// Create three more run nodes.
let run1 = new aw.Run(doc, "Run 1. ");
let run2 = new aw.Run(doc, "Run 2. ");
let run3 = new aw.Run(doc, "Run 3. ");

// The document body will not display these runs until we insert them into a composite node
// that itself is a part of the document's node tree, as we did with the first run.
// We can determine where the text contents of nodes that we insert
// appears in the document by specifying an insertion location relative to another node in the paragraph.
expect(paragraph.getText().trim()).toEqual("Initial text.");

// Insert the second run into the paragraph in front of the initial run.
paragraph.insertBefore(run2, paragraphText);

expect(paragraph.getText().trim()).toEqual("Run 2. Initial text.");

// Insert the third run after the initial run.
paragraph.insertAfter(run3, paragraphText);

expect(paragraph.getText().trim()).toEqual("Run 2. Initial text. Run 3.");

// Insert the first run to the start of the paragraph's child nodes collection.
paragraph.prependChild(run1);

expect(paragraph.getText().trim()).toEqual("Run 1. Run 2. Initial text. Run 3.");
expect(paragraph.getChildNodes(aw.NodeType.Any, true).count).toEqual(4);

// We can modify the contents of the run by editing and deleting existing child nodes.
//paragraph.getChildNodes(aw.NodeType.Run, true).toArray().at(1).text = "Updated run 2. ";
//paragraph.getChildNodes(aw.NodeType.Run, true).remove(paragraphText);
paragraph.getChildNodes(aw.NodeType.Run, true).toArray().at(1).asRun().text = "Updated run 2. ";
paragraph.getChildNodes(aw.NodeType.Run, true).remove(paragraphText);

expect(paragraph.getText().trim()).toEqual("Run 1. Updated run 2. Run 3.");
expect(paragraph.getChildNodes(aw.NodeType.Any, true).count).toEqual(3);
```

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
* class [CompositeNode](../)

