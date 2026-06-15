---
title: INodeChangingCallback class
linktitle: INodeChangingCallback class
articleTitle: INodeChangingCallback class
second_title: Aspose.Words for Python
description: "aspose.words.INodeChangingCallback class. Implement this interface if you want to receive notifications when nodes are inserted or removed in the document."
type: docs
weight: 600
url: /python-net/aspose.words/inodechangingcallback/
---

## INodeChangingCallback class

Implement this interface if you want to receive notifications when nodes are inserted or removed in the document.


### Methods

| Name | Description |
| --- | --- |
|[ node_inserted(args)](./node_inserted/#nodechangingargs) | Called when a node belonging to this document has been inserted into another node. |
|[ node_inserting(args)](./node_inserting/#nodechangingargs) | Called just before a node belonging to this document is about to be inserted into another node. |
|[ node_removed(args)](./node_removed/#nodechangingargs) | Called when a node belonging to this document has been removed from its parent. |
|[ node_removing(args)](./node_removing/#nodechangingargs) | Called just before a node belonging to this document is about to be removed from the document. |

### Examples

Shows how customize node changing with a callback (HandleNodeChangingFontChanger).

```python
class HandleNodeChangingFontChanger(aw.INodeChangingCallback):

    def __init__(self):
        self.m_log = []

    def node_inserted(self, args):
        self.m_log.append(f'\tType:\t{args.node.node_type}' + '\n')
        self.m_log.append(f'\tHash:\t{hash(args.node)}' + '\n')
        if args.node.node_type == aw.NodeType.RUN:
            font = args.node.as_run().font
            self.m_log.append(f'\tFont:\tChanged from "{font.name}" {font.size}pt')
            font.size = 24
            font.name = 'Arial'
            self.m_log.append(f' to "{font.name}" {font.size}pt' + '\n')
            self.m_log.append(f'\tContents:\n\t\t"{args.node.get_text()}"' + '\n')

    def node_inserting(self, args):
        from datetime import datetime
        # ...
        mLog.append(f'\n{datetime.now():%d/%m/%Y %H:%M:%S:%f}\tNode insertion:')

    def node_removed(self, args):
        self.m_log.append(f'\tType:\t{args.node.node_type}' + '\n')
        self.m_log.append(f'\tHash code:\t{hash(args.node)}' + '\n')

    def node_removing(self, args):
        from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
        import datetime
        # Assuming mLog is a string builder or similar object
        # For demonstration, we'll use a simple string concatenation
        mLog = ''
        mLog += '\n' + datetime.datetime.now().strftime('%d/%m/%Y %H:%M:%S:%f')[:-3] + '\tNode removal:'

    def get_log(self):
        return str.join('', self.m_log)
```

### See Also

* module [aspose.words](../)

