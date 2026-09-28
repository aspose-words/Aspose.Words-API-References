---
title: PageSetup.gutter property
linktitle: gutter property
articleTitle: gutter property
second_title: Aspose.Words for Python
description: "PageSetup.gutter property. Gets or sets the amount of extra space added to the margin for document binding."
type: docs
weight: 160
url: /ar/python-net/aspose.words/pagesetup/gutter/
---

## PageSetup.gutter property

Gets or sets the amount of extra space added to the margin for document binding.


```python
@property
def gutter(self) -> float:
    ...

@gutter.setter
def gutter(self, value: float):
    ...

```

### Examples

Shows how to set gutter margins.

```python
doc = aw.Document()
# أدرج نصًا يمتد عبر عدة صفحات.
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 6:
    builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# يضيف الفاصل مساحات بيضاء إما إلى الهامش الأيسر أو الأيمن للصفحة،
# مما يعوض الطي المركزي للصفحات في الكتاب الذي يقتحم تخطيط الصفحة.
page_setup = doc.sections[0].page_setup
# حدد مقدار المساحة المتاحة للنص داخل هوامش صفحاتنا، ثم أضف مقدارًا لتوسيع الهامش.
self.assertAlmostEqual(470.3, page_setup.page_width - page_setup.left_margin - page_setup.right_margin, delta=0.01)
page_setup.gutter = 100
# قم بتعيين الخاصية "RtlGutter" إلى "true" لوضع الفاصل في موضع أكثر ملاءمة للنص من اليمين إلى اليسار.
page_setup.rtl_gutter = True
# قم بتعيين الخاصية "MultiplePages" إلى "MultiplePagesType.MirrorMargins" لتبديل
# موضع هوامش الجانب الأيسر/الأيمن لكل صفحة.
page_setup.multiple_pages = aw.settings.MultiplePagesType.MIRROR_MARGINS
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Gutter.docx')
```

Shows how to configure a document that can be printed as a book fold.

```python
doc = aw.Document()
# أدرج نصًا يمتد عبر 16 صفحة.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('My Booklet:')
i = 0
while i < 15:
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    builder.write(f'Booklet face #{i}')
    i += 1
# قم بتكوين خاصية "PageSetup" للقسم الأول لطباعة المستند على شكل طية كتاب.
# عند طباعة هذا المستند على الوجهين، يمكننا أخذ الصفحات لتكديسها
# وطويها جميعًا من الوسط مرة واحدة. سيُرتّب محتوى المستند في طية كتاب.
page_setup = doc.sections[0].page_setup
page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# يمكننا تحديد عدد الأوراق فقط على أساس مضاعفات 4.
page_setup.sheets_per_booklet = 4
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Booklet.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

