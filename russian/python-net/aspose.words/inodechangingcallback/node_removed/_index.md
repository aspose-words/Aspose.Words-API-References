---
title: INodeChangingCallback.node_removed method
linktitle: node_removed method
articleTitle: node_removed method
second_title: Aspose.Words for Python
description: "INodeChangingCallback.node_removed method. Called when a node belonging to this document has been removed from its parent."
type: docs
weight: 30
url: /ru/python-net/aspose.words/inodechangingcallback/node_removed/
---

## node_removed(args) {#nodechangingargs}

Called when a node belonging to this document has been removed from its parent.


```python
def node_removed(self, args: aspose.words.NodeChangingArgs):
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
        # Предполагая, что mLog — это StringBuilder или аналогичный объект
        # Для демонстрации мы используем простую конкатенацию строк
        mLog = ''
        mLog += '\n' + datetime.datetime.now().strftime('%d/%m/%Y %H:%M:%S:%f')[:-3] + '\tNode removal:'

    def get_log(self):
        return str.join('', self.m_log)
```

### See Also

* module [aspose.words](../../)
* class [INodeChangingCallback](../)

