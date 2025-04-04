---
title: Node.nodeType property
linktitle: nodeType property
articleTitle: nodeType property
second_title: Aspose.Words for Node.js
description: "Node.nodeType property. Gets the type of this node."
type: docs
weight: 50
url: /nodejs-net/aspose.words/node/nodeType/
---

## Node.nodeType property

Gets the type of this node.


```js
get nodeType(): Aspose.Words.NodeType
```

### Examples

Shows how to traverse a composite node's tree of child nodes.

```js
test('RecurseChildren', () => {
  let doc = new aw.Document(base.myDir + "Paragraphs.docx");

  // Any node that can contain child nodes, such as the document itself, is composite.
  expect(doc.isComposite).toEqual(true);

  // Invoke the recursive function that will go through and print all the child nodes of a composite node.
  traverseAllNodes(doc, 0);
});


/// <summary>
/// Recursively traverses a node tree while printing the type of each node
/// with an indent depending on depth as well as the contents of all inline nodes.
/// </summary>
function traverseAllNodes(parentNode, depth)
{
  for (let childNode = parentNode.firstChild; childNode != null; childNode = childNode.nextSibling)
  {
    console.log(`${'\t'.repeat(depth)}${aw.Node.nodeTypeToString(childNode.nodeType)}`);

    // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
    if (childNode.isComposite)
    {
      traverseAllNodes(childNode.asCompositeNode(), depth + 1);
    }
    else
    {
      var text = childNode.getText().trim();
      if (text !== undefined) {
        console.log(` - \"${text}\"`);
      }
    }
  }
}
```

Shows how to remove all child nodes of a specific type from a composite node.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");

expect(doc.getChildNodes(aw.NodeType.Table, true).count).toEqual(2);

let curNode = doc.firstSection.body.firstChild;

while (curNode != null)
{
  // Save the next sibling node as a variable in case we want to move to it after deleting this node.
  let nextNode = curNode.nextSibling;

  // A section body can contain Paragraph and Table nodes.
  // If the node is a Table, remove it from the parent.
  if (curNode.nodeType == aw.NodeType.Table)
    curNode.remove();

  curNode = nextNode;
}

expect(doc.getChildNodes(aw.NodeType.Table, true).count).toEqual(0);
```

Shows how to use a node's NextSibling property to enumerate through its immediate children.

```js
let doc = new aw.Document(base.myDir + "Paragraphs.docx");

for (let node = doc.firstSection.body.firstChild; node != null; node = node.nextSibling)
{
  console.log(`Node type: ${aw.Node.nodeTypeToString(node.nodeType)}`);

  let contents = node.getText().trim();
  console.log(contents == '' ? "This node contains no text" : `Contents: \"${node.getText().trim()}\"`);
}
```

### See Also

* module [Aspose.Words](../../)
* class [Node](../)

