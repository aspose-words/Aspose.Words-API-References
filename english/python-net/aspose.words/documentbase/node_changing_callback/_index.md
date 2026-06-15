---
title: DocumentBase.node_changing_callback property
linktitle: node_changing_callback property
articleTitle: node_changing_callback property
second_title: Aspose.Words for Python
description: "DocumentBase.node_changing_callback property. Called when a node is inserted or removed in the document."
type: docs
weight: 60
url: /python-net/aspose.words/documentbase/node_changing_callback/
---

## DocumentBase.node_changing_callback property

Called when a node is inserted or removed in the document.


```python
@property
def node_changing_callback(self) -> aspose.words.INodeChangingCallback:
    ...

@node_changing_callback.setter
def node_changing_callback(self, value: aspose.words.INodeChangingCallback):
    ...

```

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
* class [DocumentBase](../)

