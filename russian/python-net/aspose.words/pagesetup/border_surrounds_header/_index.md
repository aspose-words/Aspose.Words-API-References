---
title: PageSetup.border_surrounds_header property
linktitle: border_surrounds_header property
articleTitle: border_surrounds_header property
second_title: Aspose.Words for Python
description: "PageSetup.border_surrounds_header property. Specifies whether the page border includes or excludes the header."
type: docs
weight: 60
url: /ru/python-net/aspose.words/pagesetup/border_surrounds_header/
---

## PageSetup.border_surrounds_header property

Specifies whether the page border includes or excludes the header.


```python
@property
def border_surrounds_header(self) -> bool:
    ...

@border_surrounds_header.setter
def border_surrounds_header(self, value: bool):
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
# Вставьте синюю двойную линию границы.
page_setup = doc.sections[0].page_setup
page_setup.borders.line_style = aw.LineStyle.DOUBLE
page_setup.borders.color = aspose.pydrawing.Color.blue
# Объект PageSetup раздела имеет флаги "BorderSurroundsHeader" и "BorderSurroundsFooter", определяющие
# окружает ли граница страницы основной текст, а также включает заголовок или нижний колонтитул соответственно.
# Установите флаг "BorderSurroundsHeader" в "true", чтобы окружить заголовок нашей границей,
# а затем установите флаг "BorderSurroundsFooter", чтобы оставить нижний колонтитул за пределами границы.
page_setup.border_surrounds_header = True
page_setup.border_surrounds_footer = False
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PageBorder.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

