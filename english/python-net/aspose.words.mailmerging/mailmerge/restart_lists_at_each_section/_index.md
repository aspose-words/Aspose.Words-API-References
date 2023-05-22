---
title: MailMerge.restart_lists_at_each_section property
linktitle: restart_lists_at_each_section property
articleTitle: restart_lists_at_each_section property
second_title: Aspose.Words for Python
description: "MailMerge.restart_lists_at_each_section property. Gets or sets a value indicating whether lists are restarted at each section after executing of a mail merge."
type: docs
weight: 110
url: /python-net/aspose.words.mailmerging/mailmerge/restart_lists_at_each_section/
---

## MailMerge.restart_lists_at_each_section property

Gets or sets a value indicating whether lists are restarted at each section after executing of a mail merge.

The default value is ``True``.



### Examples

Shows how to control whether or not list numbering is restarted at each section when mail merge is performed.

```python
doc = aw.Document(MY_DIR + "Section breaks with numbering.docx")

doc.mail_merge.restart_lists_at_each_section = False
doc.mail_merge.execute("", object())

doc.save(ARTIFACTS_DIR + "MailMerge.restart_lists_at_each_section.pdf")
```

### See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

