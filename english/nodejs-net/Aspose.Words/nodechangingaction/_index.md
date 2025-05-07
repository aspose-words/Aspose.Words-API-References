---
title: NodeChangingAction enumeration
linktitle: NodeChangingAction enumeration
articleTitle: NodeChangingAction enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.NodeChangingAction enumeration. Specifies the type of node change."
type: docs
weight: 830
url: /nodejs-net/aspose.words/nodechangingaction/
---

## NodeChangingAction enumeration

Specifies the type of node change.


### Members

| Name | Description |
| --- | --- |
| Insert | A node is being inserted in the tree. |
| Remove | A node is being removed from the tree. |

### Examples

Shows how to use a NodeChangingCallback to monitor changes to the document tree in real-time as we edit it.

```js
test.skip('NodeChangingCallback - TODO: WORDSNODEJS-120 - Add support of doc.nodeChangingCallback', () => {
    let doc = new aw.Document();
    doc.nodeChangingCallback = new NodeChangingPrinter();

    let builder = new aw.DocumentBuilder(doc);
    builder.writeln("Hello world!");
    builder.startTable();
    builder.insertCell();
    builder.write("Cell 1");
    builder.insertCell();
    builder.write("Cell 2");
    builder.endTable();

    builder.insertImage(base.imageDir + "Logo.jpg");            

    builder.currentParagraph.parentNode.removeAllChildren();
  });


/*    /// <summary>
    /// Prints every node insertion/removal as it takes place in the document.
    /// </summary>
  private class NodeChangingPrinter : INodeChangingCallback
  {
    void aw.INodeChangingCallback.nodeInserting(NodeChangingArgs args)
    {
      expect(args.action).toEqual(aw.NodeChangingAction.Insert);
      expect(args.oldParent).toEqual(null);
    }

    void aw.INodeChangingCallback.nodeInserted(NodeChangingArgs args)
    {
      expect(args.action).toEqual(aw.NodeChangingAction.Insert);
      expect(args.newParent).not.toBe(null);

      console.log("Inserted node:");
      console.log(`\tType:\t${args.node.nodeType}`);

      if (args.node.getText().trim() != "")
      {
        console.log(`\tText:\t\"${args.node.getText().trim()}\"`);
      }

      console.log(`\tHash:\t${args.node.getHashCode()}`);
      console.log(`\tParent:\t${args.newParent.nodeType} (${args.newParent.getHashCode()})`);
    }

    void aw.INodeChangingCallback.nodeRemoving(NodeChangingArgs args)
    {
      expect(args.action).toEqual(aw.NodeChangingAction.Remove);
    }

    void aw.INodeChangingCallback.nodeRemoved(NodeChangingArgs args)
    {
      expect(args.action).toEqual(aw.NodeChangingAction.Remove);
      expect(args.newParent).toBe(null);

      console.log(`Removed node: ${args.node.nodeType} (${args.node.getHashCode()})`);
    }
  }
```

### See Also

* module [Aspose.Words](../)
* class [NodeChangingArgs](../nodechangingargs/)
* property [NodeChangingArgs.action](../nodechangingargs/action/)

