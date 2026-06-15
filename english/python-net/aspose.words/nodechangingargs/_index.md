---
title: NodeChangingArgs class
linktitle: NodeChangingArgs class
articleTitle: NodeChangingArgs class
second_title: Aspose.Words for Python
description: "aspose.words.NodeChangingArgs class. Provides data for methods of the [INodeChangingCallback](../inodechangingcallback/) interface."
type: docs
weight: 810
url: /python-net/aspose.words/nodechangingargs/
---

## NodeChangingArgs class

Provides data for methods of the [INodeChangingCallback](../inodechangingcallback/) interface.

To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/python-net/aspose-words-document-object-model/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [action](./action/) | Gets a value indicating what type of node change event is occurring. |
| [new_parent](./new_parent/) | Gets the node's parent that will be set after the operation completes. |
| [node](./node/) | Gets the [NodeChangingArgs.node](./node/) that is being added or removed. |
| [old_parent](./old_parent/) | Gets the node's parent before the operation began. |

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
* class [DocumentBase](../documentbase/)
* class [INodeChangingCallback](../inodechangingcallback/)
* enum [NodeChangingAction](../nodechangingaction/)

