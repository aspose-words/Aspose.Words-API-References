---
title: Document.compliance property
linktitle: compliance property
articleTitle: compliance property
second_title: Aspose.Words for Python
description: "Document.compliance property. Gets the OOXML compliance version determined from the loaded document content"
type: docs
weight: 60
url: /python-net/aspose.words/document/compliance/
---

## Document.compliance property

Gets the OOXML compliance version determined from the loaded document content.
Makes sense only for OOXML documents.


```python
@property
def compliance(self) -> aspose.words.saving.OoxmlCompliance:
    ...

```

### Remarks

If you created a new blank document or load non OOXML document
returns the [OoxmlCompliance.ECMA376_2006](../../../aspose.words.saving/ooxmlcompliance/#ECMA376_2006) value.




### Examples

Shows how to read a loaded document's Open Office XML compliance version.

```python
# The compliance version varies between documents created by different versions of Microsoft Word.
doc = aw.Document(MY_DIR + "Document.doc")

self.assertEqual(doc.compliance, aw.saving.OoxmlCompliance.ECMA376_2006)

doc = aw.Document(MY_DIR + "Document.docx")

self.assertEqual(doc.compliance, aw.saving.OoxmlCompliance.ISO29500_2008_TRANSITIONAL)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

