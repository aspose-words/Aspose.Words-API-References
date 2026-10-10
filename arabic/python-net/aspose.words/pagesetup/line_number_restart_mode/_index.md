---
title: PageSetup.line_number_restart_mode property
linktitle: line_number_restart_mode property
articleTitle: line_number_restart_mode property
second_title: Aspose.Words for Python
description: "PageSetup.line_number_restart_mode property. Gets or sets the way line numbering runs  that is, whether it starts over at the beginning of a new page or section or runs continuously."
type: docs
weight: 230
url: /ar/python-net/aspose.words/pagesetup/line_number_restart_mode/
---

## PageSetup.line_number_restart_mode property

Gets or sets the way line numbering runs  that is, whether it starts over at the beginning of a new
page or section or runs continuously.


```python
@property
def line_number_restart_mode(self) -> aspose.words.LineNumberRestartMode:
    ...

@line_number_restart_mode.setter
def line_number_restart_mode(self, value: aspose.words.LineNumberRestartMode):
    ...

```

### Examples

Shows how to enable line numbering for a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# يمكننا استخدام كائن PageSetup الخاص بالقسم لعرض الأرقام إلى يسار أسطر نص القسم.
# هذا هو نفس سلوك كائن List،
# ولكنه يغطي القسم بأكمله ولا يغيّر النص بأي شكل.
# سوف يعيد قسمنا ترقيم الصفحات على كل صفحة جديدة بدءًا من 1 ويعرض الرقم،
# إذا كان مضاعفًا للرقم 3، على بعد 50pt إلى يسار السطر.
page_setup = builder.page_setup
page_setup.line_starting_number = 1
page_setup.line_number_count_by = 3
page_setup.line_number_restart_mode = aw.LineNumberRestartMode.RESTART_PAGE
page_setup.line_number_distance_from_text = 50
i = 1
while i <= 25:
    builder.writeln(f'Line {i}.')
    i += 1
# سيتخطى عداد السطر أي فقرة تحتوي على العلامة \"SuppressLineNumbers\" مضبوطة على \"true\".
# هذه الفقرة في السطر الخامس عشر، وهو مضاعف للرقم 3، وبالتالي عادةً ما يتم عرض رقم السطر.
# سيقوم عداد سطر القسم أيضًا بتجاهل هذا السطر، ويعامل السطر التالي كالسطر الخامس عشر،
# ويستمر العد من تلك النقطة فصاعدًا.
doc.first_section.body.paragraphs[14].paragraph_format.suppress_line_numbers = True
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.LineNumbers.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

