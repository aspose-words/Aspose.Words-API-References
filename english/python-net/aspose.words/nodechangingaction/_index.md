---
title: NodeChangingAction enumeration
linktitle: NodeChangingAction enumeration
articleTitle: NodeChangingAction enumeration
second_title: Aspose.Words for Python
description: "aspose.words.NodeChangingAction enumeration. Specifies the type of node change."
type: docs
weight: 800
url: /python-net/aspose.words/nodechangingaction/
---

## NodeChangingAction enumeration

Specifies the type of node change.


### Members

| Name | Description |
| --- | --- |
| INSERT | A node is being inserted in the tree. |
| REMOVE | A node is being removed from the tree. |

### Examples

Shows how to use a NodeChangingCallback to monitor changes to the document tree in real-time as we edit it (NodeChangingPrinter).

```python
class NodeChangingPrinter(aw.INodeChangingCallback):

    def node_inserting(self, args):
        self.assertEqual(aw.NodeChangingAction.INSERT, args.action)
        self.assertEqual(None, args.old_parent)

    def node_inserted(self, args):
        self.assertEqual(aw.NodeChangingAction.INSERT, args.action)
        self.assertIsNotNone(args.new_parent)
        print('Inserted node:')
        print(f'\tType:\t{args.node.node_type}')
        if args.node.get_text().strip() != '':
            print(f'\tText:\t"{args.node.get_text().strip()}"')
        print(f'\tHash:\t{hash(args.node)}')
        print(f'\tParent:\t{args.new_parent.node_type} ({hash(args.new_parent)})')

    def node_removing(self, args):
        self.assertEqual(aw.NodeChangingAction.REMOVE, args.action)

    def node_removed(self, args):
        self.assertEqual(aw.NodeChangingAction.REMOVE, args.action)
        self.assertIsNone(args.new_parent)
        print(f'Removed node: {args.node.node_type} ({hash(args.node)})')
```

### See Also

* module [aspose.words](../)
* class [NodeChangingArgs](../nodechangingargs/)
* property [NodeChangingArgs.action](../nodechangingargs/action/)

