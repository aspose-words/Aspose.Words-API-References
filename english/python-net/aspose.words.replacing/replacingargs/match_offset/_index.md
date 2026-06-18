---
title: ReplacingArgs.match_offset property
linktitle: match_offset property
articleTitle: match_offset property
second_title: Aspose.Words for Python
description: "ReplacingArgs.match_offset property. Gets the zero-based starting position of the match from the start of the node that contains the beginning of the match."
type: docs
weight: 50
url: /python-net/aspose.words.replacing/replacingargs/match_offset/
---

## ReplacingArgs.match_offset property

Gets the zero-based starting position of the match from the start of
the node that contains the beginning of the match.


```python
@property
def match_offset(self) -> int:
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
* class [ReplacingArgs](../)

