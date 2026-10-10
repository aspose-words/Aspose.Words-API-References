---
title: Paragraph.runs property
linktitle: runs property
articleTitle: runs property
second_title: Aspose.Words for Python
description: "Paragraph.runs property. Provides access to the typed collection of pieces of text inside the paragraph."
type: docs
weight: 220
url: /tr/python-net/aspose.words/paragraph/runs/
---

## Paragraph.runs property

Provides access to the typed collection of pieces of text inside the paragraph.


```python
@property
def runs(self) -> aspose.words.RunCollection:
    ...

```

### Examples

Shows how to determine the revision type of an inline node.

```python
doc = aw.Document(file_name=MY_DIR + 'Revision runs.docx')
# Belgeyi düzenlerken, Review -> Tracking üzerinden bulunan "Track Changes" seçeneği,
# Microsoft Word'de etkinleştirildiğinde, uyguladığımız değişiklikler revizyon olarak sayılır.
# Aspose.Words kullanarak bir belgeyi düzenlerken, revizyon takibini başlatabiliriz
# belgenin "StartTrackRevisions" metodunu çağırarak ve "StopTrackRevisions" metodunu kullanarak takibi durdurabilirsiniz.
# Revizyonları kabul ederek belgeye dahil edebiliriz
# ya da reddederek önerilen değişikliği etkili bir şekilde iptal edebiliriz.
self.assertEqual(6, doc.revisions.count)
# Bir revizyonun üst düğümü, revizyonun ilgili olduğu run'dur. Run, bir Inline düğümdür.
run = doc.revisions[0].parent_node.as_run()
first_paragraph = run.parent_paragraph
runs = first_paragraph.runs
self.assertEqual(6, len(list(runs)))
# Aşağıda bir Inline düğümünü işaretleyebilen beş revizyon türü bulunmaktadır.
# 1 -  Bir "insert" revizyonu:
# Bu revizyon, değişiklikleri izlerken metin eklediğimizde oluşur.
self.assertTrue(runs[2].is_insert_revision)
# 2 -  Bir "format" revizyonu:
# Bu revizyon, değişiklikleri izlerken metnin biçimini değiştirdiğimizde oluşur.
self.assertTrue(runs[2].is_format_revision)
# 3 -  Bir "move from" revizyonu:
# Microsoft Word'de metni vurguladığımızda ve ardından belge içinde farklı bir konuma sürüklediğimizde
# değişiklikleri izlerken iki revizyon ortaya çıkar.
# "move from" revizyonu, metnin taşınmadan önceki bir kopyasıdır.
self.assertTrue(runs[4].is_move_from_revision)
# 4 -  Bir "move to" revizyonu:
# "move to" revizyonu, belge içinde yeni konumunda taşınan metindir.
# "Move from" ve "move to" revizyonları, gerçekleştirdiğimiz her taşıma revizyonu için çiftler halinde görünür.
# Bir taşıma revizyonunu kabul etmek, "move from" revizyonunu ve metnini siler,
# ve "move to" revizyonundaki metni tutar.
# Bir taşıma revizyonunu reddetmek ise "move from" revizyonunu tutar ve "move to" revizyonunu siler.
self.assertTrue(runs[1].is_move_to_revision)
# 5 -  Bir "delete" revizyonu:
# Bu revizyon, değişiklikleri izlerken metin sildiğimizde oluşur. Böyle bir metni sildiğimizde,
# belge içinde bir revizyon olarak kalır, ta ki revizyonu kabul edene kadar,
# metni kalıcı olarak silecek, ya da revizyonu reddedecek; bu, sildiğimiz metni olduğu yerde tutacak.
self.assertTrue(runs[5].is_delete_revision)
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

