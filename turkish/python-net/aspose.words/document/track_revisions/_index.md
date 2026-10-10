---
title: Document.track_revisions property
linktitle: track_revisions property
articleTitle: track_revisions property
second_title: Aspose.Words for Python
description: "Document.track_revisions property. True if changes are tracked when this document is edited in Microsoft Word."
type: docs
weight: 460
url: /tr/python-net/aspose.words/document/track_revisions/
---

## Document.track_revisions property

True if changes are tracked when this document is edited in Microsoft Word.


```python
@property
def track_revisions(self) -> bool:
    ...

@track_revisions.setter
def track_revisions(self, value: bool):
    ...

```

### Remarks

Setting this option only instructs Microsoft Word whether the track changes
is turned on or off. This property has no effect on changes to the document that you make
programmatically via Aspose.Words.

If you want to automatically track changes as they are made programmatically by Aspose.Words
to this document use the [Document.start_track_revisions()](../start_track_revisions/#str_datetime) method.




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

* module [aspose.words](../../)
* class [Document](../)

