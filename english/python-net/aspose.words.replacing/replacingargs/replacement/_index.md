---
title: ReplacingArgs.replacement property
linktitle: replacement property
articleTitle: replacement property
second_title: Aspose.Words for Python
description: "ReplacingArgs.replacement property. Gets or sets the replacement string."
type: docs
weight: 60
url: /python-net/aspose.words.replacing/replacingargs/replacement/
---

## ReplacingArgs.replacement property

Gets or sets the replacement string.


```python
@property
def replacement(self) -> str:
    ...

@replacement.setter
def replacement(self, value: str):
    ...

```

### Examples

Shows how to replace all occurrences of a regular expression pattern with another string, while tracking all such replacements (TextFindAndReplacementLogger).

```python
class TextFindAndReplacementLogger(aw.replacing.IReplacingCallback):

    def __init__(self):
        self.m_log = []

    def replacing(self, args):
        m_log.append(f'"{args.match.value}" converted to "{args.replacement}" {args.match_offset} characters into a {args.match_node.node_type} node.')
        args.replacement = f'(Old value:"{args.match.value}") {args.replacement}'
        return aw.Replacing.ReplaceAction.REPLACE

    def get_log(self):
        return str.join('', self.m_log)
```

### See Also

* module [aspose.words.replacing](../../)
* class [ReplacingArgs](../)

