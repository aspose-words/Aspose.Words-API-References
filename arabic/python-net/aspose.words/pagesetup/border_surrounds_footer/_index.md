---
title: PageSetup.border_surrounds_footer property
linktitle: border_surrounds_footer property
articleTitle: border_surrounds_footer property
second_title: Aspose.Words for Python
description: "PageSetup.border_surrounds_footer property. Specifies whether the page border includes or excludes the footer."
type: docs
weight: 50
url: /ar/python-net/aspose.words/pagesetup/border_surrounds_footer/
---

## PageSetup.border_surrounds_footer property

Specifies whether the page border includes or excludes the footer.


```python
@property
def border_surrounds_footer(self) -> bool:
    ...

@border_surrounds_footer.setter
def border_surrounds_footer(self, value: bool):
    ...

```

### Remarks

Note, changing this property affects all sections in the document.


### Examples

Shows how to apply a border to the page and header/footer.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world! This is the main body text.')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('This is the header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.write('This is the footer.')
builder.move_to_document_end()
# أدرج حدًا مزدوجًا أزرق.
page_setup = doc.sections[0].page_setup
page_setup.borders.line_style = aw.LineStyle.DOUBLE
page_setup.borders.color = aspose.pydrawing.Color.blue
# كائن PageSetup في القسم يحتوي على علامات "BorderSurroundsHeader" و"BorderSurroundsFooter" التي تحدد
# ما إذا كان حد الصفحة يحيط بالنص الرئيسي للجسم، ويشمل أيضًا الرأس أو التذييل، على التوالي.
# قم بتعيين علامة "BorderSurroundsHeader" إلى "true" لإحاطة الرأس بالحد الخاص بنا،
# ثم قم بتعيين علامة "BorderSurroundsFooter" لترك التذييل خارج الحد.
page_setup.border_surrounds_header = True
page_setup.border_surrounds_footer = False
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PageBorder.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

