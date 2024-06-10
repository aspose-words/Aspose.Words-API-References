---
title: MailMerge.get_field_names method
linktitle: get_field_names method
articleTitle: get_field_names method
second_title: Aspose.Words for Python
description: "MailMerge.get_field_names method. Returns a collection of mail merge field names available in the document."
type: docs
weight: 200
url: /python-net/aspose.words.mailmerging/mailmerge/get_field_names/
---

## get_field_names() {#default}

Returns a collection of mail merge field names available in the document.


```python
def get_field_names(self):
    ...
```

### Remarks

Returns full merge field names including optional prefix. Does not eliminate duplicate field names.

A new string array is created on every call.

Includes "mustache" field names if [MailMerge.use_non_merge_fields](../use_non_merge_fields/) is ``True``.




### See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

