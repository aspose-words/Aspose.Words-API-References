---
title: RunCollection class
linktitle: RunCollection class
articleTitle: RunCollection class
second_title: Aspose.Words for Python
description: "aspose.words.RunCollection class. Provides typed access to a collection of [Run](../run/) nodes"
type: docs
weight: 1120
url: /tr/python-net/aspose.words/runcollection/
---

## RunCollection class

Provides typed access to a collection of [Run](../run/) nodes.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/python-net/programming-with-documents/) documentation article.




**Inheritance:** [RunCollection](./) → [NodeCollection](../nodecollection/)

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Retrieves a [Run](../run/) at the given index. |

### Properties

| Name | Description |
| --- | --- |
| [count](../nodecollection/count/) | Gets the number of nodes in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |

### Methods

| Name | Description |
| --- | --- |
|[ add(node)](../nodecollection/add/#node) | Adds a node to the end of the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ clear()](../nodecollection/clear/#default) | Removes all nodes from this collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ contains(node)](../nodecollection/contains/#node) | Determines whether a node is in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ index_of(node)](../nodecollection/index_of/#node) | Returns the zero-based index of the specified node.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ insert(index, node)](../nodecollection/insert/#int_node) | Inserts a node into the collection at the specified index.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ remove(node)](../nodecollection/remove/#node) | Removes the node from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ remove_at(index)](../nodecollection/remove_at/#int) | Removes the node at the specified index from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ to_array()](./to_array/#default) | Copies all runs from the collection to a new array of runs. |

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

* module [aspose.words](../)
* class [NodeCollection](../nodecollection/)

