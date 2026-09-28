---
title: PageSetup.rtl_gutter property
linktitle: rtl_gutter property
articleTitle: rtl_gutter property
second_title: Aspose.Words for Python
description: "PageSetup.rtl_gutter property. Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language."
type: docs
weight: 380
url: /ar/python-net/aspose.words/pagesetup/rtl_gutter/
---

## PageSetup.rtl_gutter property

Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language.


```python
@property
def rtl_gutter(self) -> bool:
    ...

@rtl_gutter.setter
def rtl_gutter(self, value: bool):
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

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

