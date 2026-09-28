---
title: PageSetup.line_starting_number property
linktitle: line_starting_number property
articleTitle: line_starting_number property
second_title: Aspose.Words for Python
description: "PageSetup.line_starting_number property. Gets or sets the starting line number."
type: docs
weight: 240
url: /ar/python-net/aspose.words/pagesetup/line_starting_number/
---

## PageSetup.line_starting_number property

Gets or sets the starting line number.


```python
@property
def line_starting_number(self) -> int:
    ...

@line_starting_number.setter
def line_starting_number(self, value: int):
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

