---
title: Revision class
linktitle: Revision class
articleTitle: Revision class
second_title: Aspose.Words for Python
description: "aspose.words.Revision class. Represents a revision (tracked change) in a document node or style"
type: docs
weight: 1050
url: /ru/python-net/aspose.words/revision/
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

