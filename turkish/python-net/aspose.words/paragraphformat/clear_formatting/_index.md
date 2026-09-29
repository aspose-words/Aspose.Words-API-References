---
title: ParagraphFormat.clear_formatting method
linktitle: clear_formatting method
articleTitle: clear_formatting method
second_title: Aspose.Words for Python
description: "ParagraphFormat.clear_formatting method. Resets to default paragraph formatting."
type: docs
weight: 430
url: /tr/python-net/aspose.words/paragraphformat/clear_formatting/
---

## clear_formatting() {#default}

Resets to default paragraph formatting.


```python
def clear_formatting(self):
    ...
```

### Remarks

Default paragraph formatting is Normal style, left aligned, no indentation,
no spacing, no borders and no shading.


### Examples

Shows how to nest a list inside another list.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Bir liste, paragraf gruplarını ön ek sembolleri ve girintilerle düzenlememizi ve süslememizi sağlar.
# Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
# Bir belge oluşturucusunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve sonlandırabiliriz.
# Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf, listenin bir öğesi haline gelecektir.
# Başlıklar için bir taslak (outline) listesi oluşturun.
outline_list = doc.lists.add(list_template=aw.lists.ListTemplate.OUTLINE_NUMBERS)
builder.list_format.list = outline_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('This is my Chapter 1')
# Numaralı bir liste oluşturun.
numbered_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
builder.list_format.list = numbered_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.NORMAL
builder.writeln('Numbered list item 1.')
# Bir listeyi oluşturan her paragraf bu bayrağa sahip olacaktır.
self.assertTrue(builder.current_paragraph.is_list_item)
self.assertTrue(builder.paragraph_format.is_list_item)
# Madde işaretli bir liste oluşturun.
bulleted_list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
builder.list_format.list = bulleted_list
builder.paragraph_format.left_indent = 72
builder.writeln('Bulleted list item 1.')
builder.writeln('Bulleted list item 2.')
builder.paragraph_format.clear_formatting()
# Numaralı listeye geri dönün.
builder.list_format.list = numbered_list
builder.writeln('Numbered list item 2.')
builder.writeln('Numbered list item 3.')
# Taslak listesine geri dönün.
builder.list_format.list = outline_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('This is my Chapter 2')
builder.paragraph_format.clear_formatting()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.NestedLists.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

