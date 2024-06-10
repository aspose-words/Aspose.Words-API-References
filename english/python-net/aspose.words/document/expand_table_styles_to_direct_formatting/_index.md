---
title: Document.expand_table_styles_to_direct_formatting method
linktitle: expand_table_styles_to_direct_formatting method
articleTitle: expand_table_styles_to_direct_formatting method
second_title: Aspose.Words for Python
description: "Document.expand_table_styles_to_direct_formatting method. Converts formatting specified in table styles into direct formatting on tables in the document."
type: docs
weight: 630
url: /python-net/aspose.words/document/expand_table_styles_to_direct_formatting/
---

## expand_table_styles_to_direct_formatting() {#default}

Converts formatting specified in table styles into direct formatting on tables in the document.


```python
def expand_table_styles_to_direct_formatting(self):
    ...
```

### Remarks

This method exists because this version of Aspose.Words provides only limited support for
table styles (see below). This method might be useful when you load a DOCX or WordprocessingML
document that contains tables formatted with table styles and you need to query formatting of
tables, cells, paragraphs or text.

This version of Aspose.Words provides limited support for table styles as follows:


* Table styles defined in DOCX or WordprocessingML documents are preserved as table styles
  when saving the document as DOCX or WordprocessingML.
  
* Table styles defined in DOCX or WordprocessingML documents are automatically converted
  to direct formatting on tables when saving the document into any other format,
  rendering or printing.
  
* Table styles defined in DOC documents are preserved as table styles when
  saving the document as DOC only.
  



### Examples

Shows how to apply the properties of a table's style directly to the table's elements.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Hello world!')
builder.end_table()
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
table_style.row_stripe = 3
table_style.cell_spacing = 5
table_style.shading.background_pattern_color = aspose.pydrawing.Color.antique_white
table_style.borders.color = aspose.pydrawing.Color.blue
table_style.borders.line_style = aw.LineStyle.DOT_DASH
table.style = table_style
# This method concerns table style properties such as the ones we set above.
doc.expand_table_styles_to_direct_formatting()
doc.save(ARTIFACTS_DIR + 'Document.table_style_to_direct_formatting.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

