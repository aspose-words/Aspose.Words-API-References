---
title: SmartTag.nodeType property
linktitle: nodeType property
articleTitle: nodeType property
second_title: Aspose.Words for Node.js
description: "SmartTag.nodeType property. Returns [NodeType.SmartTag](../../../aspose.words/nodetype/#SmartTag)."
type: docs
weight: 30
url: /nodejs-net/aspose.words.markup/smarttag/nodeType/
---

## SmartTag.nodeType property

Returns [NodeType.SmartTag](../../../aspose.words/nodetype/#SmartTag).



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

### See Also

* module [Aspose.Words.Markup](../../)
* class [SmartTag](../)

