---
title: FindReplaceOptions.apply_font property
linktitle: apply_font property
articleTitle: apply_font property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.apply_font property. Text formatting applied to new content."
type: docs
weight: 20
url: /python-net/aspose.words.replacing/findreplaceoptions/apply_font/
---

## FindReplaceOptions.apply_font property

Text formatting applied to new content.


```python
@property
def apply_font(self) -> aspose.words.Font:
    ...

```

### Examples

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

