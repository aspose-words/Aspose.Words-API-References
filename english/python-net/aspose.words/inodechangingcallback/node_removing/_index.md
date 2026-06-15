---
title: INodeChangingCallback.node_removing method
linktitle: node_removing method
articleTitle: node_removing method
second_title: Aspose.Words for Python
description: "INodeChangingCallback.node_removing method. Called just before a node belonging to this document is about to be removed from the document."
type: docs
weight: 40
url: /python-net/aspose.words/inodechangingcallback/node_removing/
---

## node_removing(args) {#nodechangingargs}

Called just before a node belonging to this document is about to be removed from the document.


```python
def node_removing(self, args: aspose.words.NodeChangingArgs):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| args | [NodeChangingArgs](../../nodechangingargs/) |  |

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

* module [aspose.words](../../)
* class [INodeChangingCallback](../)

