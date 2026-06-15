---
title: ReplacingArgs.match_end_node property
linktitle: match_end_node property
articleTitle: match_end_node property
second_title: Aspose.Words for Python
description: "ReplacingArgs.match_end_node property. Gets the node that contains the end of the match."
type: docs
weight: 30
url: /python-net/aspose.words.replacing/replacingargs/match_end_node/
---

## ReplacingArgs.match_end_node property

Gets the node that contains the end of the match.


```python
@property
def match_end_node(self) -> aspose.words.Node:
    ...

```

### Examples

Shows how to get match end node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('1')
builder.writeln('2')
builder.writeln('3')
replacing_callback = self.ReplacingCallback()
options = aw.replacing.FindReplaceOptions()
options.replacing_callback = replacing_callback
doc.range.replace_regex(pattern='1[\\s\\S]*3', replacement='X', options=options)
self.assertEqual('1', replacing_callback.start_node_text)
self.assertEqual('3', replacing_callback.end_node_text)
```

Shows how to get match end node.

```python
class ReplacingCallback(aw.replacing.IReplacingCallback):

    @property
    def start_node_text(self):
        pass

    @start_node_text.setter
    def start_node_text(self, value):
        pass

    @property
    def end_node_text(self):
        pass

    @end_node_text.setter
    def end_node_text(self, value):
        pass

    def replacing(self, e):
        start_node_text = e.match_node.get_text().strip()
        end_node_text = e.match_end_node.get_text().strip()
        return aw.replacing.ReplaceAction.REPLACE
```

### See Also

* module [aspose.words.replacing](../../)
* class [ReplacingArgs](../)

