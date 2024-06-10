---
title: Document.mail_merge_settings property
linktitle: mail_merge_settings property
articleTitle: mail_merge_settings property
second_title: Aspose.Words for Python
description: "Document.mail_merge_settings property. Gets or sets the object that contains all of the mail merge information for a document."
type: docs
weight: 280
url: /python-net/aspose.words/document/mail_merge_settings/
---

## Document.mail_merge_settings property

Gets or sets the object that contains all of the mail merge information for a document.


```python
@property
def mail_merge_settings(self) -> aspose.words.settings.MailMergeSettings:
    ...

@mail_merge_settings.setter
def mail_merge_settings(self, value: aspose.words.settings.MailMergeSettings):
    ...

```

### Remarks

You can use this object to specify a mail merge data source for a document and this information
(along with the available data fields) will appear in Microsoft Word when the user opens this document.
Or you can use this object to query mail merge settings that the user has specified in Microsoft Word
for this document.

This object is never ``None``.




### See Also

* module [aspose.words](../../)
* class [Document](../)

