---
title: MailMergeSettings.link_to_query property
linktitle: link_to_query property
articleTitle: link_to_query property
second_title: Aspose.Words for Python
description: "MailMergeSettings.link_to_query property. Not sure about this one"
type: docs
weight: 110
url: /python-net/aspose.words.settings/mailmergesettings/link_to_query/
---

## MailMergeSettings.link_to_query property

Not sure about this one.
The Microsoft Word Automation Reference suggests that this specifies that the query is executed every time the document 
is opened in Microsoft Word. But the OOXML specification suggests that this specifies that the query contains a reference
to an external query file which contains the actual query.
The default value is ``False``.



```python
@property
def link_to_query(self) -> bool:
    ...

@link_to_query.setter
def link_to_query(self, value: bool):
    ...

```

### See Also

* module [aspose.words.settings](../../)
* class [MailMergeSettings](../)

