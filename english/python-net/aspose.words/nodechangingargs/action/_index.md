---
title: NodeChangingArgs.action property
linktitle: action property
articleTitle: action property
second_title: Aspose.Words for Python
description: "NodeChangingArgs.action property. Gets a value indicating what type of node change event is occurring."
type: docs
weight: 10
url: /python-net/aspose.words/nodechangingargs/action/
---

## NodeChangingArgs.action property

Gets a value indicating what type of node change event is occurring.


```python
@property
def action(self) -> aspose.words.NodeChangingAction:
    ...

```

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

* module [aspose.words](../../)
* class [NodeChangingArgs](../)

