---
title: Story.last_paragraph property
linktitle: last_paragraph property
articleTitle: last_paragraph property
second_title: Aspose.Words for Python
description: "Story.last_paragraph property. Gets the last paragraph in the story."
type: docs
weight: 20
url: /tr/python-net/aspose.words/story/last_paragraph/
---

## Story.last_paragraph property

Gets the last paragraph in the story.


```python
@property
def last_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to move a DocumentBuilder's cursor position to a specified node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Run 1. ')
# Belge oluşturucu bir imlece sahiptir; bu imleç belgenin bir bölümü gibi davranır
# yapıcı, belge oluşturma yöntemlerini kullandığımızda yeni düğümler eklediği yerdir.
# Bu imleç, Microsoft Word'ün yanıp sönen imleciyle aynı şekilde çalışır,
# ve ayrıca her zaman yapıcının yeni eklediği herhangi bir düğümün hemen sonrasında bulunur.
# Belgenin farklı bir bölümüne içerik eklemek için,
# imleci \"MoveTo\" yöntemiyle farklı bir düğüme taşıyabiliriz.
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# İmleç şimdi taşındığı düğümün önündedir.
# İkinci bir çalışmanın eklenmesi, onu ilk çalışmanın önüne yerleştirir.
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# İmleci belgenin sonuna taşıyarak, daha önceki gibi metni sona eklemeye devam edin.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

