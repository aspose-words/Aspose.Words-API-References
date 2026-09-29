---
title: Paragraph.is_move_to_revision property
linktitle: is_move_to_revision property
articleTitle: is_move_to_revision property
second_title: Aspose.Words for Python
description: "Paragraph.is_move_to_revision property. Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 140
url: /tr/python-net/aspose.words/paragraph/is_move_to_revision/
---

## Paragraph.is_move_to_revision property

Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.



```python
@property
def is_move_to_revision(self) -> bool:
    ...

```

### Examples

Shows how to check whether a paragraph is a move revision.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
# Bu belge "Move" revizyonlarını içerir, bunlar imleçle metni vurguladığımızda ortaya çıkar,
# ve ardından metni başka bir konuma taşımak için sürükleriz
# Microsoft Word'de revizyonları "Review" -> "Track changes" yoluyla izlerken.
self.assertEqual(6, len(list(filter(lambda r: r.revision_type == aw.RevisionType.MOVING, doc.revisions))))
paragraphs = doc.first_section.body.paragraphs
# "Move from" ve "Move to" revizyon çiftlerinden oluşur.
# Bu revizyonlar, belgeye yapılabilecek ve kabul edebileceğimiz ya da reddedebileceğimiz potansiyel değişikliklerdir.
# Bir taşıma revizyonunu kabul etmeden/ reddetmeden önce, belge
# metnin hem çıkış hem de varış noktalarını izlemek zorundadır.
# İkinci ve dördüncü paragraf bu tür bir revizyonu tanımlar ve bu nedenle ikisinin de aynı içeriği vardır.
self.assertEqual(paragraphs[1].get_text(), paragraphs[3].get_text())
# "Move from" revizyonu, metni sürüklediğimiz paragraftır.
# Revizyonu kabul edersek, bu paragraf kaybolacaktır,
# ve diğer paragraf kalır ve artık bir revizyon olmaz.
self.assertTrue(paragraphs[1].is_move_from_revision)
# "Move to" revizyonu, metni sürüklediğimiz paragraftır.
# Revizyonu reddedersek, bu paragraf yerine kaybolur ve diğer paragraf kalır.
self.assertTrue(paragraphs[3].is_move_to_revision)
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

