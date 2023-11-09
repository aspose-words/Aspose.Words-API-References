---
title: MailMerge.trim_whitespaces property
linktitle: trim_whitespaces property
articleTitle: trim_whitespaces property
second_title: Aspose.Words for Python
description: "MailMerge.trim_whitespaces property. Gets or sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values."
type: docs
weight: 130
url: /python-net/aspose.words.mailmerging/mailmerge/trim_whitespaces/
---

## MailMerge.trim_whitespaces property

Gets or sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values.


```python
@property
def trim_whitespaces(self) -> bool:
    ...

@trim_whitespaces.setter
def trim_whitespaces(self, value: bool):
    ...

```

### Remarks

The default value is ``True``.



### Examples

Shows how to trim whitespaces from values of a data source while executing a mail merge.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.insert_field("MERGEFIELD myMergeField", None)

doc.mail_merge.trim_whitespaces = trim_whitespaces
doc.mail_merge.execute(["myMergeField"], ["\t hello world! "])

self.assertEqual("hello world!\f" if trim_whitespaces else "\t hello world! \f", doc.get_text())
```

### See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

