---
title: Revision class
linktitle: Revision class
articleTitle: Revision class
second_title: Aspose.Words for Python
description: "aspose.words.Revision class. Represents a revision (tracked change) in a document node or style"
type: docs
weight: 1050
url: /tr/python-net/aspose.words/revision/
---

## Revision class

Represents a revision (tracked change) in a document node or style.
Use [Revision.revision_type](./revision_type/) to check the type of this revision.
To learn more, visit the [Track Changes in a Document](https://docs.aspose.com/words/python-net/track-changes-in-a-document/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [author](./author/) | Gets or sets the author of this revision. Can not be empty string or ``None``. |
| [date_time](./date_time/) | Gets or sets the date/time of this revision. |
| [group](./group/) | Gets the revision group. Returns ``None`` if the revision does not belong to any group. |
| [parent_node](./parent_node/) | Gets the immediate parent node (owner) of this revision. This property will work for any revision type other than [RevisionType.STYLE_DEFINITION_CHANGE](../revisiontype/#STYLE_DEFINITION_CHANGE). |
| [parent_style](./parent_style/) | Gets the immediate parent style (owner) of this revision. This property will work for only for the [RevisionType.STYLE_DEFINITION_CHANGE](../revisiontype/#STYLE_DEFINITION_CHANGE) revision type. |
| [revision_type](./revision_type/) | Gets the type of this revision. |

### Methods

| Name | Description |
| --- | --- |
|[ accept()](./accept/#default) | Accepts this revision. |
|[ reject()](./reject/#default) | Reject this revision. |

### Examples

Shows how to work with revisions in a document.

```python
class ExRevision(ApiExampleBase):

    def test_revisions(self):
        doc = aw.Document()
        builder = aw.DocumentBuilder(doc=doc)
        # Belgenin normal düzenlemesi bir revizyon olarak sayılmaz.
        builder.write('This does not count as a revision. ')
        self.assertFalse(doc.has_revisions)
        # Düzenlemelerimizi revizyon olarak kaydetmek için bir yazar tanımlamamız ve ardından bunları izlemeye başlamamız gerekir.
        doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
        builder.write('This is revision #1. ')
        self.assertTrue(doc.has_revisions)
        self.assertEqual(1, doc.revisions.count)
        # Bu işaret, Microsoft Word'deki "Review" -> "Tracking" -> "Track Changes" seçeneğine karşılık gelir.
        # "StartTrackRevisions" yöntemi değerini etkilemez,
        # ve belge, değeri "false" olmasına rağmen programlı olarak revizyonları izlemektedir.
        # Bu belgeyi Microsoft Word ile açarsak, revizyonları izlemeyecek.
        self.assertFalse(doc.track_revisions)
        # Belge oluşturucu (builder) kullanarak metin ekledik, bu yüzden ilk revizyon ekleme tipi bir revizyondur.
        revision = doc.revisions[0]
        self.assertEqual('John Doe', revision.author)
        self.assertEqual('This is revision #1. ', revision.parent_node.get_text())
        self.assertEqual(aw.RevisionType.INSERTION, revision.revision_type)
        self.assertEqual(revision.date_time.date(), datetime.datetime.now().date())
        self.assertEqual(doc.revisions.groups[0], revision.group)
        # Bir run'ı kaldırarak silme tipi bir revizyon oluşturun.
        doc.first_section.body.first_paragraph.runs[0].remove()
        # Yeni bir revizyon eklemek, onu revizyon koleksiyonunun başına koyar.
        self.assertEqual(aw.RevisionType.DELETION, doc.revisions[0].revision_type)
        self.assertEqual(2, doc.revisions.count)
        # Ekleme revizyonları, revizyonu kabul/reddetmeden önce bile belge gövdesinde görünür.
        # Revizyonu reddetmek, düğümlerini gövde dışına kaldırır. Aksine, silme revizyonlarını oluşturan düğümler
        # Ayrıca revizyonu kabul edene kadar belgede kalırlar.
        self.assertEqual('This does not count as a revision. This is revision #1.', doc.get_text().strip())
        # Silme revizyonunu kabul etmek, üst düğümünü paragraf metninden kaldıracaktır
        # ve ardından koleksiyonun revizyonunu da kaldırır.
        doc.revisions[0].accept()
        self.assertEqual(1, doc.revisions.count)
        self.assertEqual('This is revision #1.', doc.get_text().strip())
        builder.writeln('')
        builder.write('This is revision #2.')
        # Şimdi düğümü taşıyarak bir hareketli revizyon türü oluşturun.
        node = doc.first_section.body.paragraphs[1]
        end_node = doc.first_section.body.paragraphs[1].next_sibling
        reference_node = doc.first_section.body.paragraphs[0]
        while node != end_node:
            next_node = node.next_sibling
            doc.first_section.body.insert_before(node, reference_node)
            node = next_node
        self.assertEqual(aw.RevisionType.MOVING, doc.revisions[0].revision_type)
        self.assertEqual(8, doc.revisions.count)
        self.assertEqual('This is revision #2.\rThis is revision #1. \rThis is revision #2.', doc.get_text().strip())
        # Hareketli revizyon şu anda 1. indekste. İçeriğini atmak için revizyonu reddedin.
        doc.revisions[1].reject()
        self.assertEqual(6, doc.revisions.count)
        self.assertEqual('This is revision #1. \rThis is revision #2.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../)

