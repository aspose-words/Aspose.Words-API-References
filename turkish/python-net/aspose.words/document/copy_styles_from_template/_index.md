---
title: Document.copy_styles_from_template method
linktitle: copy_styles_from_template method
articleTitle: copy_styles_from_template method
second_title: Aspose.Words for Python
description: "aspose.words.Document.copy_styles_from_template method"
type: docs
weight: 620
url: /tr/python-net/aspose.words/document/copy_styles_from_template/
---

## copy_styles_from_template(template) {#str}

Copies styles from the specified template to a document.


```python
def copy_styles_from_template(self, template: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| template | str |  |

### Remarks

When styles are copied from a template to a document,
like-named styles in the document are redefined to match the style descriptions in the template.
Unique styles from the template are copied to the document. Unique styles in the document remain intact.


## copy_styles_from_template(template) {#document}

Copies styles from the specified template to a document.


```python
def copy_styles_from_template(self, template: aspose.words.Document):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| template | [Document](../) |  |

### Remarks

When styles are copied from a template to a document,
like-named styles in the document are redefined to match the style descriptions in the template.
Unique styles from the template are copied to the document. Unique styles in the document remain intact.


## Examples

Shows how to copy styles from one document to another.

```python
# Bir belge oluşturun ve ardından başka bir belgeye kopyalayacağımız stilleri ekleyin.
template = aw.Document()
style = template.styles.add(aw.StyleType.PARAGRAPH, 'TemplateStyle1')
style.font.name = 'Times New Roman'
style.font.color = aspose.pydrawing.Color.navy
style = template.styles.add(aw.StyleType.PARAGRAPH, 'TemplateStyle2')
style.font.name = 'Arial'
style.font.color = aspose.pydrawing.Color.deep_sky_blue
style = template.styles.add(aw.StyleType.PARAGRAPH, 'TemplateStyle3')
style.font.name = 'Courier New'
style.font.color = aspose.pydrawing.Color.royal_blue
self.assertEqual(7, template.styles.count)
# Stilleri kopyalayacağımız bir belge oluşturun.
target = aw.Document()
# Şablon belgesindeki bir stil ile aynı ada sahip bir stil oluşturun ve hedef belgeye ekleyin.
style = target.styles.add(aw.StyleType.PARAGRAPH, 'TemplateStyle3')
style.font.name = 'Calibri'
style.font.color = aspose.pydrawing.Color.orange
self.assertEqual(5, target.styles.count)
# Bir belgeden diğerine tüm stilleri kopyalamak için yöntemi çağırmanın iki yolu vardır.
# 1 -  Şablon belge nesnesini geçirme:
target.copy_styles_from_template(template=template)
# Stilleri kopyalamak, şablon belgesindeki tüm stilleri hedefe ekler
# ve aynı ada sahip mevcut stillerin üzerine yazar.
self.assertEqual(7, target.styles.count)
self.assertEqual('Courier New', target.styles.get_by_name('TemplateStyle3').font.name)
self.assertEqual(aspose.pydrawing.Color.royal_blue.to_argb(), target.styles.get_by_name('TemplateStyle3').font.color.to_argb())
# 2 -  Şablon belgesinin yerel sistem dosya adını geçirme:
target.copy_styles_from_template(template=MY_DIR + 'Rendering.docx')
self.assertEqual(21, target.styles.count)
```

Shows how to copies styles from the template to a document via Document.

```python
template = aw.Document(file_name=MY_DIR + 'Rendering.docx')
target = aw.Document(file_name=MY_DIR + 'Document.docx')
target.copy_styles_from_template(template=template)
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

