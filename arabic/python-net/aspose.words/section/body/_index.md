---
title: Section.body property
linktitle: body property
articleTitle: body property
second_title: Aspose.Words for Python
description: "Section.body property. Returns the [Body](../../body/) child node of the section."
type: docs
weight: 20
url: /ar/python-net/aspose.words/section/body/
---

## Section.body property

Returns the [Body](../../body/) child node of the section.



```python
@property
def body(self) -> aspose.words.Body:
    ...

```

### Remarks

[Body](../../body/) contains main text of the section.

Returns ``None`` if the section does not have a [Body](../../body/) node among its children.




### Examples

Clears main text from all sections from the document leaving the sections themselves.

```python
doc = aw.Document()
# المستند الفارغ يحتوي على قسم واحد، جسم واحد وفقرة واحدة.
# استدعِ طريقة "RemoveAllChildren" لإزالة جميع تلك العقد،
# وانتهي بعقدة مستند بدون أي أطفال.
doc.remove_all_children()
# هذا المستند الآن لا يحتوي على أي عقد فرعية مركبة يمكننا إضافة محتوى إليها.
# إذا أردنا تحريره، سنحتاج إلى إعادة ملء مجموعة العقد الخاصة به.
# أولاً، أنشئ قسمًا جديدًا، ثم أضفه كطفل إلى عقدة المستند الجذرية.
section = aw.Section(doc)
doc.append_child(section)
# القسم يحتاج إلى جسم، سيحتوي ويعرض جميع محتوياته
# على الصفحة بين رأس وتذييل القسم.
body = aw.Body(doc)
section.append_child(body)
# هذا الجسم لا يحتوي على عناصر فرعية، لذا لا يمكننا إضافة مقاطع نصية إليه بعد.
self.assertEqual(0, doc.first_section.body.get_child_nodes(aw.NodeType.ANY, True).count)
# استدعِ "EnsureMinimum" للتأكد من أن هذا الجسم يحتوي على فقرة فارغة واحدة على الأقل.
body.ensure_minimum()
# الآن، يمكننا إضافة مقاطع نصية إلى الجسم، وجعل المستند يعرضها.
body.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Section](../)

