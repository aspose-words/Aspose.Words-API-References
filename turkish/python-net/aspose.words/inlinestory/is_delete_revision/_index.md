---
title: InlineStory.is_delete_revision property
linktitle: is_delete_revision property
articleTitle: is_delete_revision property
second_title: Aspose.Words for Python
description: "InlineStory.is_delete_revision property. Returns true if this object was deleted in Microsoft Word while change tracking was enabled."
type: docs
weight: 30
url: /tr/python-net/aspose.words/inlinestory/is_delete_revision/
---

## InlineStory.is_delete_revision property

Returns true if this object was deleted in Microsoft Word while change tracking was enabled.


```python
@property
def is_delete_revision(self) -> bool:
    ...

```

### Examples

Shows how to view revision-related properties of InlineStory nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Revision footnotes.docx')
# Belgeyi düzenlerken, Review -> Tracking üzerinden bulunan "Track Changes" seçeneği,
# Microsoft Word'de etkinleştirildiğinde, uyguladığımız değişiklikler revizyon olarak sayılır.
# Aspose.Words kullanarak bir belgeyi düzenlerken, revizyon takibini başlatabiliriz
# belgenin "StartTrackRevisions" metodunu çağırarak ve "StopTrackRevisions" metodunu kullanarak takibi durdurabilirsiniz.
# Revizyonları kabul ederek belgeye dahil edebiliriz
# veya önerilen değişikliği geri almak ve iptal etmek için reddedin.
self.assertTrue(doc.has_revisions)
footnotes = list(map(lambda x: x.as_footnote(), list(doc.get_child_nodes(aw.NodeType.FOOTNOTE, True))))
self.assertEqual(5, len(footnotes))
# Aşağıda, bir InlineStory düğümünü işaretleyebilen beş revizyon türü bulunmaktadır.
# 1 -  Bir "insert" revizyonu:
# Bu revizyon, değişiklikleri izlerken metin eklediğimizde oluşur.
self.assertTrue(footnotes[2].is_insert_revision)
# 2 -  "move from" revizyonu:
# Microsoft Word'de metni vurguladığımızda ve ardından belge içinde farklı bir konuma sürüklediğimizde
# değişiklikleri izlerken iki revizyon ortaya çıkar.
# "move from" revizyonu, metnin taşınmadan önceki bir kopyasıdır.
self.assertTrue(footnotes[4].is_move_from_revision)
# 3 -  "move to" revizyonu:
# "move to" revizyonu, belge içinde yeni konumunda taşınan metindir.
# "Move from" ve "move to" revizyonları, gerçekleştirdiğimiz her taşıma revizyonu için çiftler halinde görünür.
# Bir taşıma revizyonunu kabul etmek, "move from" revizyonunu ve metnini siler,
# ve "move to" revizyonundaki metni tutar.
# Bir taşıma revizyonunu reddetmek ise "move from" revizyonunu tutar ve "move to" revizyonunu siler.
self.assertTrue(footnotes[1].is_move_to_revision)
# 4 -  "delete" revizyonu:
# Bu revizyon, değişiklikleri izlerken metin sildiğimizde oluşur. Böyle bir metni sildiğimizde,
# belge içinde bir revizyon olarak kalır, ta ki revizyonu kabul edene kadar,
# metni kalıcı olarak silecek, ya da revizyonu reddedecek; bu, sildiğimiz metni olduğu yerde tutacak.
self.assertTrue(footnotes[3].is_delete_revision)
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

