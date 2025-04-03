---
title: CompositeNode.firstChild property
linktitle: firstChild property
articleTitle: firstChild property
second_title: Aspose.Words for NodeJs
description: "CompositeNode.firstChild property. Gets the first child of the node."
type: docs
weight: 20
url: /nodejs-net/aspose.words/compositenode/firstChild/
---

## CompositeNode.firstChild property

Gets the first child of the node.


```js
get firstChild(): Aspose.Words.Node
```

### Remarks

If there is no first child node, a ``null`` is returned.



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
* class [CompositeNode](../)

