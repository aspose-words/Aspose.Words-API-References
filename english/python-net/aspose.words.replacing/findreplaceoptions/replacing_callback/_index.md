---
title: FindReplaceOptions.replacing_callback property
linktitle: replacing_callback property
articleTitle: replacing_callback property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.replacing_callback property. The user-defined method which is called before every replace occurrence."
type: docs
weight: 170
url: /python-net/aspose.words.replacing/findreplaceoptions/replacing_callback/
---

## FindReplaceOptions.replacing_callback property

The user-defined method which is called before every replace occurrence.


```python
@property
def replacing_callback(self) -> aspose.words.replacing.IReplacingCallback:
    ...

@replacing_callback.setter
def replacing_callback(self, value: aspose.words.replacing.IReplacingCallback):
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

Shows how to apply a different font to new content via FindReplaceOptions (NumberHexer).

```python
class NumberHexer(aw.replacing.IReplacingCallback):

    def __init__(self):
        self.m_current_replacement_number = None
        self.m_log = []

    def replacing(self, args):
        self.m_current_replacement_number += 1
        number = int(args.match.value)
        args.replacement = f'0x{number:X}'
        self.m_log.append(f'Match #{self.m_current_replacement_number}\n')
        self.m_log.append(f'\tOriginal value:\t{args.match.value}\n')
        self.m_log.append(f'\tReplacement:\t{args.replacement}\n')
        self.m_log.append(f'\tOffset in parent {args.match_node.node_type} node:\t{args.match_offset}\n')
        self.m_log.append(f'\tGroup index:\t{args.group_index}\n' if args.group_name is None or args.group_name == '' else f'\tGroup name:\t{args.group_name}\n')
        return aw.ReplaceAction.REPLACE

    def get_log(self):
        return str.join('', self.m_log)
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

