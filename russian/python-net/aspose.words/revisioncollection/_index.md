---
title: RevisionCollection class
linktitle: RevisionCollection class
articleTitle: RevisionCollection class
second_title: Aspose.Words for Python
description: "aspose.words.RevisionCollection class. A collection of [Revision](../revision/) objects that represent revisions in the document"
type: docs
weight: 1060
url: /ru/python-net/aspose.words/revisioncollection/
---

## RevisionCollection class

A collection of [Revision](../revision/) objects that represent revisions in the document.
To learn more, visit the [Track Changes in a Document](https://docs.aspose.com/words/python-net/track-changes-in-a-document/) documentation article.




### Remarks

You do not create instances of this class directly. Use the [Document.revisions](../document/revisions/) property to get revisions present in a document.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Returns a [Revision](../revision/) at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of revisions in the collection. |
| [groups](./groups/) | Collection of revision groups. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(criteria)](./accept/#irevisioncriteria) | Accepts revisions that match specified criteria. |
|[ accept_all()](./accept_all/#default) | Accepts all revisions in this collection. |
|[ reject(criteria)](./reject/#irevisioncriteria) | Rejects revisions that match specified criteria. |
|[ reject_all()](./reject_all/#default) | Rejects all revisions in this collection. |

### Examples

Shows how to work with revisions in a document.

```python
class ExRevision(ApiExampleBase):

    def test_revisions(self):
        doc = aw.Document()
        builder = aw.DocumentBuilder(doc=doc)
        # Обычное редактирование документа не считается правкой.
        builder.write('This does not count as a revision. ')
        self.assertFalse(doc.has_revisions)
        # Чтобы зарегистрировать наши правки как ревизии, нам нужно указать автора и затем начать их отслеживание.
        doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
        builder.write('This is revision #1. ')
        self.assertTrue(doc.has_revisions)
        self.assertEqual(1, doc.revisions.count)
        # Этот флаг соответствует параметру "Review" -> "Tracking" -> "Track Changes" в Microsoft Word.
        # Метод "StartTrackRevisions" не влияет на его значение,
        # и документ программно отслеживает правки, несмотря на то, что значение равно "false".
        # Если открыть этот документ в Microsoft Word, он не будет отслеживать правки.
        self.assertFalse(doc.track_revisions)
        # Мы добавили текст с помощью document builder, поэтому первая правка является правкой типа вставки.
        revision = doc.revisions[0]
        self.assertEqual('John Doe', revision.author)
        self.assertEqual('This is revision #1. ', revision.parent_node.get_text())
        self.assertEqual(aw.RevisionType.INSERTION, revision.revision_type)
        self.assertEqual(revision.date_time.date(), datetime.datetime.now().date())
        self.assertEqual(doc.revisions.groups[0], revision.group)
        # Удалите run, чтобы создать правку типа удаления.
        doc.first_section.body.first_paragraph.runs[0].remove()
        # Добавление новой правки помещает её в начало коллекции правок.
        self.assertEqual(aw.RevisionType.DELETION, doc.revisions[0].revision_type)
        self.assertEqual(2, doc.revisions.count)
        # Вставленные правки отображаются в теле документа даже до того, как мы примем/отклоним правку.
        # Отклонение ревизии удалит её узлы из тела. Напротив, узлы, составляющие удалённые ревизии
        # также остаются в документе, пока мы не примем ревизию.
        self.assertEqual('This does not count as a revision. This is revision #1.', doc.get_text().strip())
        # Принятие удалённой ревизии удалит её родительский узел из текста абзаца
        # а затем удалит саму ревизию коллекции.
        doc.revisions[0].accept()
        self.assertEqual(1, doc.revisions.count)
        self.assertEqual('This is revision #1.', doc.get_text().strip())
        builder.writeln('')
        builder.write('This is revision #2.')
        # Теперь переместите узел, чтобы создать тип перемещающейся ревизии.
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
        # Перемещающаяся ревизия теперь находится на индексе 1. Отклоните ревизию, чтобы избавиться от её содержимого.
        doc.revisions[1].reject()
        self.assertEqual(6, doc.revisions.count)
        self.assertEqual('This is revision #1. \rThis is revision #2.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../)

